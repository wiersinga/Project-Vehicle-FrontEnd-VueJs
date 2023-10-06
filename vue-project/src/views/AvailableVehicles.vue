<template>

  <CustomHeader />
<h2>Les véhicules disponibles : </h2>

  <div class="vehiclesList">
    <div class="vehicle" v-for="vehicle in vehicles" :key="vehicle.id">
      <div class="vehicle-container">
        <p style="font-size: 30px; font-weight: bold">{{ vehicle.brand }}, {{ vehicle.model }}</p>
        <p style="font-weight: lighter">{{ vehicle.fiscalHPower }} Chevaux Fiscaux</p>
        <img :src="vehicle.image" height="250" width="250">
        <p>Prix par journée: {{ vehicle.priceDay }} £</p>
      </div>
    </div>
  </div>
</template>

<script>
import CustomHeader from "@/components/CustomHeader.vue";
import axios from 'axios';

export default {
  name: 'AvailableVehicles',
  data() {
    return {

      vehicles: [],
      myComponent: false
    }
  },
  created() {
    // axios.get('')
    //     .then(response=>{
    //       this.vehicles=response.data;
    //     })
    //     .catch.error('Erreur lors de la récupération des données de API',error);
    this.fetchDataFromAPI();
  },
  methods: {
    fetchDataFromAPI() {
      axios.get(`http://localhost:8080/vehicle`)
          .then(response => {
            this.vehicles = response.data;
          })
          .catch(error => {
            console.error('Erreur lors de la récupération des données de l\'API:', error);
          });
    },
    components: {
    }
  }
}

</script>


<style>
.vehicle-container{
  border: black 2px solid;
  width: 280px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.vehiclesList{
  display: flex;
  flex-direction: row;
  gap: 20px;
}
</style>
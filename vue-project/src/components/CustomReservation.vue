<template>
<div class="containerReser">

  <div class="typeVehicle">
    <div class="car-type">
      <img src="./icons/voiture.png">
      <a href="#"> Véhicules</a>
    </div>

    <div class="moto-type">
      <img src="./icons/moto.png">
      <a href="#"> Moto</a>
    </div>

    <div class="truck-type">
      <img src="./icons/camion.png">
      <a href="#"> Utilitaires</a>
    </div>
  </div>

  <div class="pickUp-return-date">
    <div class="datePick">
      <label for="datePick">Date de départ</label>
      <input type="date" id="datePick" v-model="selectedPickDate" />
    </div>

    <div class="dateReturn">
      <label for="dateReturn">Date de départ</label>
      <input type="date" id="dateReturn" v-model="selectedReturnDate" />
    </div>
    <!--      <p>{{ selectedDate }}</p>-->
  </div>

</div>
</template>

<style scoped>
.containerReser {
  margin-top: 50px;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  text-align: center;
  border: 2px solid black;
  width: 55%;
  min-height: 150px;
}
.typeVehicle {
  display: flex;
  justify-content: start;
  align-items: start;
  gap: 20px; /* Espace entre les images */
  padding-bottom: 20px;
}
.datePick, .dateReturn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}
.car-type , .moto-type , .truck-type{
  display: flex;
  justify-content: center;
  align-items: center; /* Pour aligner verticalement le contenu */
  gap: 10px; /* Espacement horizontal entre l'image et le lien */
  border: 1px black solid;
  border-radius: 40px;
  width: 150px;
  background-color: bisque;
}
.pickUp-return-date{
  display: flex;
  justify-content: space-around;
  gap: 50px;
}
</style>



<script>
export default {
  data() {
  return {
  selectedPickDate: '',
    selectedReturnDate: ''
};
}
}

</script>
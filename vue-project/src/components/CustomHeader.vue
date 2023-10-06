<template>
  <div class="headerBox">


      <div class="headerLeft">

        <div class="headerLogo">
          <img width="100" height="60" src="./icons/bird3.png">
          <p>Drive Free</p>
        </div>
        <a href="#">Louer</a>
        <a href="#">Abonnement</a>
      </div>



    <div class="headerRight">
      <a href="#"><img src="./icons/langue-icone.png" width="40" height="40"></a>
      <a href="#">Inscription/Connexion</a>
    </div>
  </div>
  <div class="imgHeader">
    <CustomReservation/>
  </div>
  <div>
    <CustomPromotions/>
  </div>
  <div>
    <CustomMap/>
  </div>
  <div>
    <CustomFooter/>
  </div>
</template>

<script>
import CustomReservation from "@/components/CustomReservation.vue";
import CustomPromotions from "@/components/CustomPromotions.vue";

import CustomMap from "@/components/CustomMap.vue";
import axios from "axios";
import CustomFooter from "./CustomFooter.vue";

export default {
  name: 'CustomHeader',
  components: {
    CustomMap,
    CustomPromotions,
    CustomReservation,
    CustomFooter
  },
  created() {
    axios.get('http://localhost:9090/reservation');
  }
};
</script>

<style scoped>
.headerBox {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #ffffff;
  padding: 10px 20px;
  color: black;
  height: 60px;
  border-radius: 5px;
}

.headerLeft {
  display: flex;
  text-align-all: start;
  align-items: center;

}

.headerLogo {
  display: flex;
  flex-direction: column;
  text-align: center;
  padding-top: 0;
}
.headerLogo p{
  margin-top: 0px;
  margin-bottom: 15px;
  font-weight: bold;
  color: rgb(0, 100, 0);
  display: flex;
  flex-direction: column;
}

.headerRight {
  display: flex;
  align-items: center;
}

.headerLeft a,
.headerRight a {
  margin-left: 20px;
  text-decoration: none;
  color: black;
  font-family: system-ui;
  font-size: 25px;
  font-weight: bold;
}

.headerLeft a:hover,
.headerRight a:hover {
//text-decoration: underline; color: #C9E3CC;
}


</style>
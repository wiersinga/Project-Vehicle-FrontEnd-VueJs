<template>
  <div class="headerBox">
    <div class="headerLeft">
      <img width="120" height="120" src="./icons/bird-logo.jpg">
      <a href="#">Louer</a>
      <a href="#">Abonnement</a>
    </div>
    <div class="headerRight">
      <a href="#"><img src="./icons/langue-icone.png"></a>
      <a href="#">Inscription/Connexion</a>
    </div>
  </div>
  <div class="imgHeader">
<!--    <img src="./icons/carO.jpg">-->
    <CustomReservation />
  </div>
</template>
<!--     <h1>Header Page</h1>-->

<script>
import CustomReservation from "@/components/CustomReservation.vue";

export default {
  name: 'CustomHeader',
  components: {CustomReservation},
  // components : {
  //   CustomHeader
  // }
}
</script>

<style scoped>
.headerBox {
  display: flex;
  justify-content: space-around;
  align-items: center;
  background-color: #ffffff;
  padding: 10px 20px;
  color: black;
  height: 80px;
  border-radius: 5px;
}
.headerLeft {
  display: flex;
  align-items: center;
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
  //text-decoration: underline;
  color: blueviolet;
}


</style>
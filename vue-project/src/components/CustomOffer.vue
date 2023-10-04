<template>
<div class="offersContainer">
  <div class="oneOfferContainer">
    <div>
      <img :src="offerImage" class="offerImage">
      <h4>{{ offerTitle }}</h4>
      <p>{{ offerDescription }}</p>
    </div>
    <div>
      <a href="#" class="orderOfferClick" style="font-size: 16px; font-weight: bold; color:darkgreen; text-decoration: none">Réservez Maintenant </a>
    </div>
  </div>
</div>

</template>

<style scoped>
.orderOfferClick:hover {
  color: red;
}
.offersContainer {
  display: flex;
  flex-direction: row;
  flex: 0.3;
}
.oneOfferContainer{
  display: flex;
  flex-direction: column;
}

.offerImage{
  width: 100%;
  height: 200px;
}

</style>

<script>
export default {
props : {
      offerImage :String,
      offerDescription:String,
      offerTitle:String
    },
};
</script>
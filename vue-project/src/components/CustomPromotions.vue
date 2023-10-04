<template>
<div class="offers">
  <div>
    <h3>Explorez les offres et produits <span  class="colored-text">Drive Free</span></h3>
  </div>
  <div class="offersWrapper">
    <CustomOffer v-for="(offer, index) in offers"
                 :key="index" :offer-image="offer.offerImage"
                 :offer-title="offer.offerTitle"
                 :offer-description="offer.offerDescription"
    />

  </div>
</div>
</template>

<style scoped>
.colored-text {
  color: darkgreen;
}
h3 {
  font-weight: bold;
  font-size: 32px;
}
.offers{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}
.offersWrapper{
  display: flex;
  flex-direction: row;
  gap: 15px;
  justify-content: center;
}
</style>

<script>
import CustomOffer from "@/components/CustomOffer.vue";

export default {
  components: {CustomOffer},
  data(){
    return {
      offers :[ {
        offerImage : '/offerImg1.png',
        offerTitle:'DRIVE FREE+ pour les entreprises !',
        offerDescription:'Découvrez vos avantages exculsifs en tant que professionnel'
      },{
        offerImage : '/offerImg2.jpg',
        offerTitle:'Abonnez-vous à lynk & Co 01',
        offerDescription:'Lynk & Co 01 à partir de 809£/mois avec DRIVE FREE+'
      },{
        offerImage : '/offerImg3.jpg',
        offerTitle:'Besoin dun chauffeur ?',
        offerDescription:'Maintenant vous avez la possibilité de réserver un véhicule ainsi qu\'un Chauffeur porfessionnel'
      }
      ]
    }
  }
}
</script>

<template>
  <div>
    <div class="footerBox">
      <div class="footerTop">

        <div class="insurance">
          <img src="./icons/assurance.png" width="100" height="70">
          <p>Annulation gratuite</p>
          <p>Voir nos conditions</p>
        </div>

        <div class="commitment">
          <img src="./icons/engagements.png" width="125" height="70">
          <p>Nos engagements</p>
          <p>+ Proche, - Cher</p>
        </div>

        <div class="payment">
          <img src="./icons/paiment.png" width="100" height="70">
          <p>Paiement 100% sécurisé </p>
          <p>Réservez en toute sécurité</p>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.footerTop {
  display: flex;
  justify-content: center;
  gap: 150px;
  margin-top: 60px;
}

.footerBox {
  background-color: #e5efe5;
}

.insurance {
  text-align: center;
}
.commitment{
  text-align: center;
}
.payment{
  text-align: center;
}



</style>
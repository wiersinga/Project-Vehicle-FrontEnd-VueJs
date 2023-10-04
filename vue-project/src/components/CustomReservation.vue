<template>
  <div class="img-Reser-Container" :style="{backgroundImage: `url(${ backgroundReser})`,backgroundSize: 'cover', backgroundPosition: '50% 40%'}">

    <div class="ageInput">
      <label for="ageInput">Entrez votre age </label>
      <select name="ageSelect" id="ageSelect">
        <option value="">--choisissez votre age !--</option>
        <option value="20">18-20</option>
        <option value="25">21-25</option>
        <option value="26">+26</option>
      </select>
    </div>

    <div class="containerReser" >

      <div class="typeVehicle">

        <div class="car-type" @click="changeBackground('/carT.jpg'), changeButtonReservation('Voir les voitures')">
          <img src="./icons/voiture.png" height="30" width="30">
          <a>Voitures</a>
        </div>

        <div class="moto-type" @click="changeBackground('/motos.jpg'), changeButtonReservation('Voir les motos')">
          <img src="./icons/moto.png" height="30" width="30">
          <a>Motos</a>
        </div>

        <div class="truck-type" @click="changeBackground('/utilitaires.jpg'), changeButtonReservation('Voir les utilitaires')">
          <img src="./icons/camion.png" height="30" width="30">
          <a>Utilitaires</a>
        </div>

      </div>

      <div class="pickUp-return-date">
        <div class="datePick">
          <label for="datePick" style="font-size: 20px">Date de départ</label>
          <div class="date-input">
            <input type="date" id="datePick" v-model="selectedPickDate" required="required"/>
            <i class="far fa-calendar-alt"></i>
          </div>
        </div>

        <div class="dateReturn">
          <label for="dateReturn" style="font-size: 20px">Date de retour</label>
          <div class="date-input">
            <input type="date" id="dateReturn" v-model="selectedReturnDate" required="required"/>
            <i class="far fa-calendar-alt"></i>
          </div>
        </div>
        <!--      <p>{{ selectedDate }}</p>-->
      </div>

      <div class="buttonReservation">
        <button @click="changeButtonReservation('Voir les véhicules')">{{buttonClickName}}</button>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      selectedPickDate: '',
      selectedReturnDate: '',
      selectedVehicleType: '',
      backgroundReser: '/carT.jpg',
      buttonClickName:'Voir les véhicules'
    };
  },
  methods: {
    changeBackground(imagePath) {
      this.backgroundReser = imagePath;
    },
    changeButtonReservation(buttonName){
      this.buttonClickName = buttonName;
    }

  }
};
</script>

<style scoped>
.containerReser {
  display: flex;
  justify-content: center;
  flex-direction: column;
  text-align: center;
  align-items: center;
//border: 2px solid black;
  width: 30%; min-height: 160px;
  background-color: white;
}

.ageInput {
  margin-top: -160px;
//border: 2px solid black;
  padding: 15px; background-color: white;
  font-size: 18px;
}
#ageSelect {
  width: 100px;
}

.img-Reser-Container {
  //background-image: url("");
  background-size: cover; background-position: 50% 40%;
  width: 100%;
//height: 100vh; height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 5px;
}

.typeVehicle {
  display: flex;
  justify-content: center;
  gap: 20px; /* Espace entre les images */
  padding-bottom: 20px;
  margin-left: 20px;
  margin-top: 20px
}


.datePick, .dateReturn {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.car-type, .moto-type, .truck-type {
  display: flex;
  justify-content: center;
  align-items: center; /* Pour aligner verticalement le contenu */
  gap: 10px; /* Espacement horizontal entre l'image et le lien */
  border: 1px black solid;
  border-radius: 40px;
  width: 130px;
  background-color: #C9E3CC;
  height: 40px;
  text-decoration: none;
}

.pickUp-return-date {
  display: flex;
  justify-content: space-around;
  gap: 50px;
}

.buttonReservation {
  margin-top: 20px;
  margin-bottom: 20px;
}

.date-input {
  position: relative;
  display: inline-flex;
  align-items: center;
}

.date-input input {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  outline: none;
}

.date-input i {
  position: absolute;
  right: 10px;
  font-size: 20px;
  color: #555;
  cursor: pointer;
}

button {
  background-color: #C9E3CC; /* Green */
  border: none;
  color: black;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
</style>



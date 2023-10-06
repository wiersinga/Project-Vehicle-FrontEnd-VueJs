<template>
  <div class="containerMap">
    <h3> Trouvez une agence <span style="color: darkgreen">DRIVE FREE </span>à coté</h3>

    <div style="height:500px; width:800px" class="classMap">
      <l-map ref="map" v-model:zoom="zoom" :center="[48.85817716082615, 2.3434301596567875]" :use-global-leaflet="false">
        <l-tile-layer
            url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
            layer-type="base"
            name="OpenStreetMap"
        ></l-tile-layer>
      </l-map>
    </div>
  </div>
</template>

<script>
import "leaflet/dist/leaflet.css";
import { LMap, LTileLayer } from "@vue-leaflet/vue-leaflet";

export default {
  components: {
    LMap,
    LTileLayer,
  },
  data() {
    return {
      zoom: 5,
    };
  },
};
</script>

<style scoped>
.containerMap {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
</style>





<template>
  <div class="containerMap">
    <h3> Trouvez une agence <span style="color: darkgreen">DRIVE FREE </span>à coté</h3>
  </div>
  <div class="map-container" ref="mapContainer"></div>
</template>

<script>
import { ref, onMounted, watchEffect } from "vue";
import "leaflet/dist/leaflet.css";
import L from "leaflet";

export default {
  props: {
    center: {
      type: Array,
      required: true,
    },
    zoom: {
      type: Number,
      required: true,
    },
  },
  setup(props) {
    const mapContainer = ref(null);
    let map = null;

    onMounted(() => {
      map = L.map(mapContainer.value).setView(props.center, props.zoom);

      L.tileLayer("https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png", {
        attribution: "&copy; <a href='https://www.openstreetmap.org/copyright'>OpenStreetMap</a> contributors",
      }).addTo(map);

      // Écoutez les changements de la position du centre de la carte
      watchEffect(() => {
        map.setView(props.center, props.zoom);
      });
    });

    return {
      mapContainer,
    };
  },
};
</script>

<style scoped>
.map-container {
  height: 100%;
  width: 100%;
}
</style>

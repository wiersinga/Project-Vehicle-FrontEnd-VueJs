<script setup>
import { RouterView } from 'vue-router'
import CustomHeader from "@/components/CustomHeader.vue";
import AvailableVehicles from "@/views/AvailableVehicles.vue";
import CustomFooter from "@/components/CustomFooter.vue";

</script>

<template>
  <header>
<CustomHeader />
  </header>
  <main>
  </main>


  <RouterView />
  <CustomFooter/>
</template>

<style scoped>

</style>

<script setup>
import { RouterView } from 'vue-router'
import CustomHeader from "@/components/CustomHeader.vue";

</script>

<template>
  <header>
<CustomHeader />
  </header>
  <main></main>


  <RouterView />
</template>

<style scoped>

</style>

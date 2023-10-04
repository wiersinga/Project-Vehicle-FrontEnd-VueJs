<script setup>
import { RouterView } from 'vue-router'
import CustomHeader from "@/components/CustomHeader.vue";

</script>

<template>
  <header>
<CustomHeader />
  </header>
<!--    <div class="wrapper">-->
<!--      <HelloWorld msg="You did it!" />-->

<!--&lt;!&ndash;      <nav>&ndash;&gt;-->
<!--&lt;!&ndash;        <RouterLink to="/">Home</RouterLink>&ndash;&gt;-->
<!--&lt;!&ndash;        <RouterLink to="/about">About</RouterLink>&ndash;&gt;-->
<!--&lt;!&ndash;      </nav>&ndash;&gt;-->
<!--    </div>-->


  <RouterView />
</template>

<style scoped>

</style>

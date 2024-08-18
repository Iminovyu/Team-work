<template>
  <div>
    <NavComponent />
  
   <section class="main-info">
    <MainInfoComponent></MainInfoComponent>
   </section> 
    <router-view />
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
import NavComponent from './components/NavComponent.vue';
import MainInfoComponent from './components/MainInfoComponent.vue'
</script>

<style lang="scss" scoped>

</style>
<template>
  <div>
    <NavComponent />
  
   <section class="main-info">
    
   </section> 
    <router-view />
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router';
import NavComponent from './components/NavComponent.vue';

</script>

<style lang="scss" scoped>

</style>
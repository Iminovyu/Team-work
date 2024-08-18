<template>
  <div>
    <NavComponent />
    <HeroComponent />
    <MainComponent />
<router-view />
  </div>
</template>

<script setup>
import { RouterLink , RouterView } from 'vue-router';
import NavComponent from './components/NavComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
import MainComponent from './components/MainComponent.vue';
</script>

<style lang="scss" scoped>

</style>
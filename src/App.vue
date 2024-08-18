<template>
  <div>
    <NavComponent />
    <HeroComponent />
<router-view />
  </div>
</template>

<script setup>
import { RouterLink , RouterView } from 'vue-router';
import NavComponent from './components/NavComponent.vue';
import HeroComponent from './components/HeroComponent.vue';
</script>

<style lang="scss" scoped>

</style>
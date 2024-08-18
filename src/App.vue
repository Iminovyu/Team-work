<template>
  <div>
    <registercomponent/>
    <footercomponent/>
<router-view />
  </div>
</template>

<script setup>
import { RouterLink , RouterView } from 'vue-router';
import registercomponent from './components/registercomponent.vue';
import Footercomponent from './components/Footercomponent.vue';
</script>

<style lang="scss" scoped>

</style>
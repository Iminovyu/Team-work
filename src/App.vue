<template>
  <div>
<<<<<<< HEAD
    <section class="main-info">
      <div class="container">
        <div class="product-filter">
          <div class="product-count">
            <h1>Найденно товаров: <span>245</span></h1>
          </div>
          <div class="product-types">
            <label for="radio">
              <input type="radio" name="product-type" id="radio" checked>
              <span>Все</span>
            </label>
            <label for="radio2">
              <input type="radio" name="product-type" id="radio2">
              <span>Новинки</span>
            </label>
            <label for="radio3">
              <input type="radio" name="product-type" id="radio3">
              <span>Со скидкой</span>
            </label>
          </div>
          <div class="product-select">
            <select name="select" class="select">
              <option value="Сначало дешевле">Сначало дешевле</option>
              <option value="Сначало дороже">Сначало дороже</option>
            </select>
          </div>
        </div>
      </div>
    </section>
=======
    <NavComponent />
<router-view />
>>>>>>> d4c651f0e83a8faac9b3324e447c564faceb851a
  </div>
</template>

<script setup>
import { RouterLink , RouterView } from 'vue-router';
import NavComponent from './components/NavComponent.vue';
</script>

<style lang="scss" scoped>

</style>
<template>
      <div>
            <div class="container">
                  <div class="product-filter">
                        <div class="product-count">
                              <h1>Найденно товаров: <span>245</span></h1>
                        </div>
                        <div class="product-types">
                              <label for="radio">
                                    <input type="radio" name="product-type" id="radio" checked>
                                    <span class="custom-radio"></span>
                                    <span>Все</span>
                              </label>
                              <label for="radio2">
                                    <input type="radio" name="product-type" id="radio2">
                                    <span class="custom-radio"></span>
                                    <span>Новинки</span>
                              </label>
                              <label for="radio3">
                                    <input type="radio" name="product-type" id="radio3">
                                    <span class="custom-radio"></span>
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
                  <div class="left-nav">
                        <div class="product-sections">
                              <router-link to="/">Все товары</router-link>
                              <router-link to="/">Афганские скороварки</router-link>
                              <router-link to="/">Казаны и котлы</router-link>
                              <router-link to="/">Учаги</router-link>
                              <router-link to="/">Кастрюли</router-link>
                              <router-link to="/">Мантоварки</router-link>
                              <router-link to="/">Сковороды</router-link>
                              <router-link to="/">Термосы</router-link>
                              <router-link to="/">Чайники и френч-прессы</router-link>
                              <router-link to="/">Сервировочная посуда</router-link>
                              <router-link to="/">Столовые приборы</router-link>
                              <router-link to="/">Бытовая техника</router-link>
                              <router-link to="/">Бытовая химия</router-link>
                              <router-link to="/">Товары для дома и сада</router-link>
      
      
                        </div>
                        <div class="filter-byPrice">
                              <div class="sec-control">
                                    <h1>Цена</h1>
                                    <transition name="rotate">
                                          <div class="img">
                                                <img src="@/assets/images/arrow.svg" alt="arrow">
                                          </div>
                                    </transition>
                              </div>
                              <transition class="appear">
                                    <div class="hidenshow">
                                          <p>от <span>0</span> до <span>5000</span></p>
                                          <div class="slider">
                                                <div class="min"></div>
                                                <div class="max"></div>
                                          </div>
                                    </div>
                              </transition>
                        </div>
                  </div>
            </div>
            <div class="cards" v-if="(cards)">
                  <div class="item" v-for="(card ) in cards" :key="card.id">
                        <div class="card-img">
                              <img :src="item.url" alt="card">
                        </div>
                        <div class="card-info">
                              <h1>{{ item.title }}</h1>
                              <p>{{ item.desc }}</p>
                        </div>
                        <div class="item" v-for="item in items" :key="item"></div>
                        <div class="card-img">
                              <img :src="item.url" alt="card">
                        </div>
                        <div class="card-info">
                              <h1>title</h1>
                              <p>desc</p>
                        </div>
                  </div>
            </div>
      </div>
</template>

<script setup>
import axios from 'axios';
import { ref } from 'vue';

const cards = ref([]);

axios.get('https://full-api.onrender.com/api/product/get')
  .then((res) => {
    cards.value = res.data.data
    console.log(res.data.data);
  })
  .catch((err) => {
    console.log(err)
  })
</script>

<style lang="scss" scoped>

</style>

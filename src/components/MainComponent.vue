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
                                                <img src="@/assets/images/svg/arrow.svg" alt="arrow">
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
            <div class="cards">
                <div class="card" v-for="card in cards" :key="card">
                    <img :src="card.url" alt="">
                    <p>{{ card.name }}</p>
                    <div class="price">
                        <p>{{ card.oldprice }}</p>
                        <p>{{ card.newprice }}</p>
                    </div>
                </div>
            </div>

</div>
</template>

<script setup>
import { ref } from 'vue';
import axios from 'axios'
const cards = ref([])

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

$red-color: rgba(245, 85, 85, 1);
$gray-color: rgba(196, 196, 196, 1);
.product-filter {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    background: rgba(255, 255, 255, 1);

    .product-count {
        h1 {
            font-size: 16px;
            font-weight: 300;
            line-height: 19.09px;
            text-align: left;

            span {
                font-size: 16px;
                font-weight: 400;
                line-height: 19.09px;
                text-align: left;

            }
        }

    }

    .product-types {
        display: flex;
        gap: 40px;
        align-items: center;
        text-align: center;

        label {
            font-size: 16px;
            font-weight: 300;
            line-height: 19.09px;
            text-align: left;
            display: flex;
            gap: 5px;
            cursor: pointer;

            input[type="radio"] {
                display: none;

                &:checked+.custom-radio {
                    background-color: $red-color;
                    border-color: $red-color;
                }
            }

            .custom-radio {
                width: 16px;
                height: 16px;
                border: 2px solid #999;
                border-radius: 50%;
                position: relative;
                cursor: pointer;

                &::after {
                    content: '';
                    width: 8px;
                    height: 8px;
                    background-color: transparent;
                    border-radius: 50%;
                    position: absolute;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    transition: background-color 0.2s ease;
                }
            }

            input[type="radio"]:checked+.custom-radio::after {
                background-color: white;
            }
        }
    }

    .product-select {
        select {
            background: #fff;
            outline: none;
            border: #fff;
            padding: 10px;

        }
    }
}

.left-nav {
    margin-top: 24px;
    border: 1px solid $gray-color;
    display: flex;
    flex-direction: column;
    background: #fff;
    width: 212px;
    .product-sections {
        display: flex;
        padding: 20px;
        flex-direction: column;
        gap: 13px;
        align-items: left;
        text-align: left;
        width: inherit;
        padding-bottom: 20px;
        border-bottom: 1px solid $gray-color;
        a {
            font-size: 14px;
            font-weight: 700;
            line-height: 22px;
            text-align: left;
            text-decoration: none;
            color: #000;

            &:hover {
                color: $red-color;
            }
        }
    }
    .filter-byPrice{
        display: flex;
        flex-direction: column;
        padding: 20px;
        gap: 13px;
        align-items: left;
        text-align: left;
        width: inherit;
        padding-bottom: 20px;
        border-bottom: 1px solid $gray-color;
        h1{
            font-size: 14px;
            font-weight: 700;
            line-height: 22px;
            text-align: left;
            text-decoration: none;
            color: #000;
        }
        .sec-control{
            display: flex;
            align-items: center;
            gap: 10px;
            .img{

            }
        }
    }
}
</style>
<template>
    <div class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-left">
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-1.svg" alt="">
                        </div>
                        <p>Большой асортимент
                            и выбор товаров</p>
                    </div>
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-2.svg" alt="">
                        </div>
                        <p>Предлогаем только качественные товары</p>
                    </div>
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-3.svg" alt="">
                        </div>
                        <p>Работаем напрямую
                            с производителями</p>
                    </div>
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-4.svg" alt="">
                        </div>
                        <p>Предоставляем гарантию на все товары</p>
                    </div>
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-5.svg" alt="">
                        </div>
                        <p>Бесплатная доставка товаров на дом</p>
                    </div>
                    <div class="item">
                        <div class="icon">
                            <img src="@/assets/images/svg/hero-icon-6.svg" alt="">
                        </div>
                        <p>Безопастная система
                            онлайн-оплаты</p>
                    </div>
                </div>
                <div class="hero-right"></div>
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.hero {
    &-content {
        display: flex;
        align-items: flex-start;
    }

    &-left {
        display: flex;
        max-width: 397px;
        gap: 30px;
        flex-wrap: wrap;

        .item {
            max-width: 182px;
            display: flex;
            flex-direction: column;
            align-items: center;

            .icon {
                img {
                    width: 63px;
                    height: 70px;
                }
            }

            p {
                color: #565656;
                font-family: 'Inter', sans-serif;
                font-size: 14px;
                font-weight: 500;
                line-height: 14.64px;
                text-align: center;
            }
        }
    }
}
</style>
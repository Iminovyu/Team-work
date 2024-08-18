<template>
    <div class="nav">
        <div class="container">
            <div class="nav-content">
                <div class="logo">
                    <img src="../assets/images/svg/logo.svg" alt="logo">
                </div>
                <div class="nav-right">
                    <button class="cateorogi">
                        <svg width="25" height="15" viewBox="0 0 25 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <line y1="1" x2="25" y2="1" stroke="white" stroke-width="2" />
                            <line y1="7.5" x2="25" y2="7.5" stroke="white" stroke-width="2" />
                            <line y1="14" x2="25" y2="14" stroke="white" stroke-width="2" />
                        </svg>
                        Каталог товаров
                    </button>
                    <div class="search">
                        <div class="input">
                            <input type="text" placeholder="Введите артикул или название товара...">
                        </div>
                        <button class="search-btn"><svg width="16" height="15" viewBox="0 0 16 15" fill="none"
                                xmlns="http://www.w3.org/2000/svg">
                                <g clip-path="url(#clip0_2925_23766)">
                                    <path
                                        d="M14.7954 13.6553L11.2646 10.1631C12.1265 9.12305 12.6419 7.7959 12.6419 6.3457C12.6419 3.02051 9.91388 0.322266 6.55194 0.322266C3.18704 0.322266 0.458984 3.02051 0.458984 6.34863C0.458984 9.67676 3.18704 12.375 6.55194 12.375C8.0152 12.375 9.35997 11.8652 10.4115 11.0127L13.9393 14.502C14.1763 14.7363 14.5584 14.7363 14.7954 14.502C15.0323 14.2676 15.0323 13.8896 14.7954 13.6553ZM1.6675 6.34863C1.6675 3.68262 3.8535 1.52051 6.54898 1.52051C9.24445 1.52051 11.4305 3.68262 11.4305 6.34863C11.4305 9.01465 9.24445 11.1768 6.54898 11.1768C3.8535 11.1768 1.6675 9.01465 1.6675 6.34863Z"
                                        fill="#333333" />
                                </g>
                                <defs>
                                    <clipPath id="clip0_2925_23766">
                                        <rect width="15.1657" height="15" fill="white" transform="translate(0.132812)" />
                                    </clipPath>
                                </defs>
                            </svg>
                        </button>
                    </div>
                    <div class="cycles">
                        <div class="item">
                            <img src="../assets/images/svg/vk.svg" alt="">
                        </div>
                        <div class="item">
                            <img src="../assets/images/svg/tg.svg" alt="">
                        </div>
                        <div class="item">
                            <img src="../assets/images/svg/w.svg" alt="">
                        </div>
                        <div class="item">
                            <img src="../assets/images/svg/heart.svg" alt="">
                        </div>
                        <div class="item">
                            <img src="../assets/images/svg/korzinka.svg" alt="">
                        </div>
                    </div>
                    <button class="login" @click="OpenModal">
                        Зарегистрироваться
                    </button>
                    <div class="bg-modal hidden"></div>
                    <div class="modal hidden" >
                        <div class="logo">
                            <img src="../assets/images/svg/logo.svg" alt="">
                            <button class="close-btn" @click="CloseModal">
                                <img src="../assets/images/svg/closee.svg" alt="">
                            </button>
                        </div>
                        <hr>
                        <from class="form">
                            <h2>Имя</h2>
                            <div class="input">
                                <input type="text" placeholder="Имя">
                            </div>
                            <h2>Фамилия</h2>
                            <div class="input">
                                <input type="text" placeholder="Фамилия">
                            </div>
                            <h2>Имя пользователя</h2>
                            <div class="input">
                                <input type="text" placeholder="Имя пользователя">
                            </div>
                            <h2>пароль</h2>
                            <div class="input">
                                <input type="text" placeholder="пароль">
                            </div>
                            <router-link to="/">если у вас есть учетная запись</router-link>
                            <button class="submit" type="submit">Зарегистрироваться</button>
                        </from>
                    </div>
                </div>
            </div>
            <div class="nav-bottom">
                <ul class="nav-list">
                    <li><router-link to="/">Главная</router-link></li>
                    <li><router-link to="/">Акции</router-link></li>
                    <li><router-link to="/">Распродажа</router-link></li>
                    <li><router-link to="/">Оплата и доставка</router-link></li>
                    <li><router-link to="/">Гарантия и возврат</router-link></li>
                    <li><router-link to="/">О нас</router-link></li>
                    <li><router-link to="/">Контакты</router-link></li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script setup>
    
const CloseModal = function(){
    const modal = document.querySelector('.modal')
    const bgModal = document.querySelector('.bg-modal')
    modal.classList.add('hidden')
    bgModal.classList.add('hidden')
}
const OpenModal = function(){
    const modal = document.querySelector('.modal')
    const bgModal = document.querySelector('.bg-modal')
    modal.classList.remove('hidden')
    bgModal.classList.remove('hidden')
    
}
</script>

<style lang="scss" scoped>
.nav {
    padding: 12px 0;

    &-content {
        display: flex;
        gap: 60px;
        align-items: center;
    }

    &-right {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;

        .cateorogi {
            background: #E24C55;
            display: flex;
            align-items: center;
            gap: 15px;
            border: 0;
            outline: none;
            font-family: 'Inter', sans-serif;
            font-size: 16px;
            color: #fff;
            line-height: 19.09px;
            padding: 10px 16px;
            cursor: pointer;
        }

        .search {
            max-width: 418px;
            width: 100%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 10px;
            margin-left: 30px;
            border: 1px solid #CECDCD;

            &-btn {
                border-left: 1px solid #CECDCD;
                border-right: 0px;
                border-top: 0px;
                border-bottom: 0px;
                padding: 13px 12px 12px 16px;
                outline: none;
                background: #ECECEC;
                display: grid;
                place-items: center;
            }

            .input {
                min-width: 289px;
                padding: 12px 0 11px 8px;

                input {
                    width: 100%;
                    border: none;
                    outline: none;
                    font-family: 'Inter', sans-serif;
                    font-size: 14px;
                    font-weight: 400;
                    line-height: 16.71px;
                    color: #ADADAD;
                }
            }
        }

        .cycles {
            display: flex;
            align-items: center;
            gap: 22px;

            .item {
                display: flex;
            }
        }

        .login {
            color: #fff;
            padding: 12px 8px;
            margin-left: 15px;
            background: #E24C55;
            border-radius: 8px;
            border: 0;
            outline: 0;
            font-family: "Inter", sans-serif;
            font-size: 13px;
            font-weight: 700;
            line-height: 15.73px;
            text-align: left;
            cursor: pointer;
        }
        .bg-modal{
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: #D9D9D980;
            z-index: 99;
        }
        .modal {
            position: fixed;
            width: 500px;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background: #FFFFFF;
            z-index: 999;

            .submit {
                padding: 13px 0px;
                background: #E24C55;
                cursor: pointer;
                border: 0;
                outline: 0;
                font-family: "Inter", sans-serif;
                font-size: 13px;
                font-weight: 700;
                line-height: 15.73px;
                color: #fff;
            }

            .form {
                padding: 20px 20px;
                display: flex;
                align-content: flex-start;
                flex-direction: column;

                h2 {
                    margin-bottom: 4px;
                    font-family: "Inter", sans-serif;
                    font-size: 16px;
                    font-weight: 700;
                    line-height: 15.73px;
                }

                .input {
                    padding: 17px 10px;
                    border: 1px solid #CECDCD;
                    margin-bottom: 15px;

                    input {
                        width: 100%;
                        color: #999999;
                        border: 0;
                        outline: 0;
                        font-family: "Inter", sans-serif;
                        font-size: 13px;
                        font-weight: 700;
                        line-height: 15.73px;
                    }
                }

                a {
                    text-decoration: none;
                    font-family: "Inter", sans-serif;
                    font-size: 13px;
                    font-weight: 700;
                    line-height: 15.73px;
                    color: #0094FF;
                    margin-bottom: 40px;
                }
            }

            .logo {
                padding: 4px 15px 5px 15px;
                display: flex;
                align-items: center;
                justify-content: space-between;

                img {
                    width: 120px;
                    height: 40px;
                }

                .close-btn {
                    width: 30px;
                    height: 20px;
                    border: 0;
                    outline: 0;

                    img {
                        width: inherit;
                        height: inherit;
                        pointer-events: none;
                    }
                }
            }
        }
    }

    &-bottom {
        padding: 30px 0 30px 0;
        display: flex;
        align-items: center;
        justify-content: center;

        ul {
            display: flex;
            align-items: center;
            gap: 100px;
            list-style: none;

            li {
                a {
                    text-decoration: none;
                    font-family: 'Inter', sans-serif, ;
                    font-size: 16px;
                    font-weight: 600;
                    line-height: 19.09px;
                    color: #333333;
                }
            }
        }
    }
}
</style>
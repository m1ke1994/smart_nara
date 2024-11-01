<template>
    <header class='flex flex-col'>
        <div class="flex items-center justify-between p-4 lg:p-6">
            <div class="menu flex items-center gap-4 lg:gap-10">
                <div class="logo flex p-2 lg:p-4 items-center">
                    <img class="cursor-pointer w-8 lg:w-10" src="/logo.png" alt="">
                    <p class="logo-text text-black text-lg lg:text-2xl font-bold">Smart <span>Nara</span></p>
                </div>
                <nav class="hidden lg:block">
                    <ul class="flex gap-4 lg:gap-10 text-base lg:text-lg items-center cursor-pointer">
                        <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                            <Nuxtlink to="/">Главная </Nuxtlink>
                        </li>
                        <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                            <Nuxtlink to="#">Контакты </Nuxtlink>
                        </li>
                        <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                            <Nuxtlink to="/information">Полезная информация</Nuxtlink>
                        </li>
                        <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                            <Nuxtlink to="/rewiew"> Написать отзыв</Nuxtlink>
                        </li>
                        <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                            <Nuxtlink to="#">Создать заявку</Nuxtlink>
                        </li>

                    </ul>
                </nav>
            </div>

            <div class="icons p-2 lg:p-4 max-lg:hidden">
                <ul class="flex gap-2 lg:gap-4 cursor-pointer">
                    <li><NuxtLink to="#"><img class="opacity-50 cursor-pointer hover:opacity-100 transition-all duration-500 w-6 lg:w-5"
                            src="/iconsearch.png" alt=""></NuxtLink></li>
                    <li><NuxtLink to="#"><img class="opacity-50 cursor-pointer hover:opacity-100 transition-all duration-500 w-6 lg:w-5"
                            src="/iconcart.png" alt=""></NuxtLink></li>
                    <li><NuxtLink to="/registration"><img class="opacity-50 cursor-pointer hover:opacity-100 transition-all duration-500 w-6 lg:w-5"
                            src="/iconuser.png" alt=""></NuxtLink></li>
                </ul>
            </div>

            <!-- Бургер-меню для маленьких экранов -->
            <div class="lg:hidden transition-all duration-500">
                <button @click="toggleMenu" class="text-black focus:outline-none ">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                        xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M4 6h16M4 12h16M4 18h16"></path>
                    </svg>
                </button>
            </div>
        </div>

        <!-- Мобильное меню -->
        <transition name="menu">
            <div v-if="isMenuOpen" class="lg:hidden bg-white shadow-lg p-4 transition-all duration-500">
                <ul class="flex flex-col gap-4 text-base items-center cursor-pointer">
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="#">Контакты</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="/rewiew">Отзывы</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="#">Полезная информация</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="#">Создать заявку на ремонт</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="#">Корзина</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="/registration">Регистрация</Nuxtlink>
                    </li>
                    <li class="opacity-50 hover:opacity-100 transition-all duration-500">
                        <Nuxtlink to="/login">Вход</Nuxtlink>
                    </li>
                </ul>
            </div>
        </transition>
    </header>
</template>

<script>
export default {
    data() {
        return {
            isMenuOpen: false,
        };
    },
    methods: {
        toggleMenu() {
            this.isMenuOpen = !this.isMenuOpen;
        },
    },
};
</script>

<style>
span {
    color: rgb(8, 109, 18);
}

;
</style>
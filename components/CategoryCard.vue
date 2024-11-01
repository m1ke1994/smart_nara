<script setup>
const cards = [
    {
        img: "/microvolnovka.png",
        title: "Микроволновая печь",
        alt: "Микроволновки",
        link: "/category/microwaves"
    },
    {
        img: "/cam.png",
        title: "Камеры видеонаблюдения",
        alt: "Камеры",
        link: "/category/сamers"
    },
    {
        img: "/pulesos.png",
        title: "Пылесосы",
        alt: "Пылесосы",
        link: "/category/vacuums"
    },
    {
        img: "/iphone.png",
        title: "Смартфоны",
        alt: "Smartfones",
        link: "/category/smartfones"
    },
    {
        img: "/airpods.png",
        title: "Беспроводные наушники",
        alt: "Беспроводные наушники",
        link: "/category/wireless-headphones"
    },
    {
        img: "/laptop.png",
        title: "Планшеты",
        alt: "Планшеты",
        link: "/category/tablets"
    },
    {
        img: "/computer.png",
        title: "Ноутбуки",
        alt: "Ноутбуки",
        link: "/category/laptops"
    },
    {
        img: "/watch.png",
        title: "Смарт-часы",
        alt: "Смарт-часы",
        link: "/category/smartwatches"
    },
    {
        img: "/fen.png",
        title: "Фены",
        alt: "Фены",
        link: "/category/hairdryers"
    }
];

</script>
<template>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 m-10">
        <NuxtLink v-for="(card, index) in cards" :key="index" :to="card.link" class="card w-full text-black p-6 m-2 flex flex-col items-center cursor-pointer hover:-translate-y-2 hover:shadow-2xl transition rounded-3xl border border-1 hover:text-lime-700 transition-all duration-500">
            <div class="flex flex-col justify-between h-full w-full">
                <img class="m-auto" :src="card.img" :alt="card.alt" width="150px">
                <p class="card-text text-xl text-center mt-4 hover:text-lime-700 transition-all duration-500">{{ card.title }}</p>
            </div>
        </NuxtLink>
    </div>
</template>
        

<style scoped>

</style>
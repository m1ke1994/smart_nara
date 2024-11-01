<script setup lang="ts">
const items = [
    '/1.jpg',
    '/5.jpg',
    '/2.jpg',
    '/3.jpg',
    '/4.jpg',
    '/6.jpg',
    '/7.jpg',
    
    
]
</script>
<template>
    <div class="slide  w-4/6 m-auto p-10">
            <UCarousel v-slot="{ item }" :items="items" :ui="{ item: 'basis-full' }" class="rounded-lg overflow-hidden "
                arrows>
                <img :src="item" class="w-full" draggable="false">
            </UCarousel>
        </div>
</template>
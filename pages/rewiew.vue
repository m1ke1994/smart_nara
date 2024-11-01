<template>
    <div class="reviews-container p-8 bg-gray-100 rounded-lg shadow-md m-auto w-1/2">
      <h2 class="text-2xl font-bold mb-6">Оставьте отзыв</h2>
      <div class="m-auto">
        <form @submit.prevent="submitReview">
        <div class="mb-4">
          <label for="category" class="block text-gray-700 font-bold mb-2">Категория</label>
          <select v-model="selectedCategory" id="category" class="block w-full border border-gray-300 rounded px-4 py-2 focus:outline-none focus:border-teal-500">
            <option v-for="category in categories" :key="category.link" :value="category">{{ category.title }}</option>
          </select>
        </div>
        <div class="mb-4">
          <label for="brand" class="block text-gray-700 font-bold mb-2">Бренд</label>
          <input v-model="brand" id="brand" type="text" class="block w-full border border-gray-300 rounded px-4 py-2 focus:outline-none focus:border-teal-500" placeholder="Введите бренд">
        </div>
        <div class="mb-4">
          <label for="username" class="block text-gray-700 font-bold mb-2">Имя пользователя</label>
          <input v-model="username" id="username" type="text" class="block w-full border border-gray-300 rounded px-4 py-2 focus:outline-none focus:border-teal-500" placeholder="Введите ваше имя">
        </div>
        <div class="mb-4">
          <label for="rating" class="block text-gray-700 font-bold mb-2">Оценка</label>
          <select v-model="rating" id="rating" class="block w-full border border-gray-300 rounded px-4 py-2 focus:outline-none focus:border-teal-500">
            <option value="1">1 звезда</option>
            <option value="2">2 звезды</option>
            <option value="3">3 звезды</option>
            <option value="4">4 звезды</option>
            <option value="5">5 звезд</option>
          </select>
        </div>
        <div class="mb-4">
          <label for="description" class="block text-gray-700 font-bold mb-2">Описание</label>
          <textarea v-model="description" id="description" class="block w-full border border-gray-300 rounded px-4 py-2 focus:outline-none focus:border-teal-500" placeholder="Введите ваш отзыв"></textarea>
        </div>
        <button type="submit" class="block w-1/5 py-2 text-center text-white bg-teal-500 border border-teal-500 rounded hover:bg-transparent hover:text-teal-500 transition uppercase font-roboto font-medium">Отправить отзыв</button>
      </form>
      </div>
      
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        categories: [
          { img: "/microvolnovka.png", title: "Микроволновая печь", alt: "Микроволновки", link: "/microwaves" },
          { img: "/cam.png", title: "Камеры видеонаблюдения", alt: "Камеры", link: "/Camers" },
          { img: "/pulesos.png", title: "Пылесосы", alt: "Пылесосы", link: "/vacuums" },
          { img: "/iphone.png", title: "Apple", alt: "Apple", link: "/apple" },
          { img: "/airpods.png", title: "Беспроводные наушники", alt: "Беспроводные наушники", link: "/wireless-headphones" },
          { img: "/laptop.png", title: "Планшеты", alt: "Планшеты", link: "/tablets" },
          { img: "/computer.png", title: "Ноутбуки", alt: "Ноутбуки", link: "/laptops" },
          { img: "/watch.png", title: "Смарт-часы", alt: "Смарт-часы", link: "/smartwatches" },
          { img: "/fen.png", title: "Фены", alt: "Фены", link: "/hairdryers" },
          { img: "/Android.png", title: "Android", alt: "Android", link: "/android" }
        ],
        selectedCategory: null,
        brand: '',
        username: '',
        rating: 5,
        description: ''
      };
    },
    methods: {
      submitReview() {
        const review = {
          category: this.selectedCategory.title,
          brand: this.brand,
          username: this.username,
          rating: this.rating,
          description: this.description
        };
        console.log('Отзыв отправлен:', review);
        // Здесь можно добавить логику для отправки отзыва на сервер
      }
    }
  };
  </script>
  
  <style scoped>
  /* Дополнительные стили по необходимости */
  </style>
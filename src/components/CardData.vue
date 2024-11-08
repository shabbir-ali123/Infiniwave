<template>
  
    <!-- <h2 class="text-center text-3xl font-bold mb-8">3 Phases Pour Élever Votre Présence  Digitale </h2> -->
    <div class="p-6 w-full rounded-lg shadow-md border-2 border-white rounded-2xl">
      <div class="flex py-4">
        <div class="w-[80px] h-[80px] bg-[#0E0729] rounded-full flex items-center justify-center">
          <!-- Render the icon slot here -->
          <slot name="icon"></slot>
        </div>
        <h3 class="text-xl font-semibold mt-6 ml-2">{{ title }}</h3>
      </div>
      <ul class="list-disc ml-4 text-gray-600">
        <li v-for="(item, index) in items" :key="index" class="flex items-center">
          <!-- Add icon next to each list item -->
          <img src="../assets/Arrow - Right 2.png" alt="arrow icon" class="mr-2" />
          {{ item }}
        </li>
      </ul>
    </div>
  
  </template>
  
  <script>
  export default {
    name: "CardData",
    props: {
      title: {
        type: String,
        required: true,
      },
      items: {
        type: Array,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any scoped styling if needed */
  </style>
  
<template>
    <div class="p-6 w-full rounded-lg shadow-md border-2 border-white rounded-2xl font-poppins">
      <div class="flex py-4">
        <div class="w-[60px] h-[60px] md:w-[80px] md:h-[80px] bg-[#0E0729] rounded-full flex items-center justify-center">
         
          <slot name="icon"></slot>
        </div>
        <h3 class="text-[32px] md:text-[38px] font-black mt-2 ml-2">{{ title }}</h3>
      </div>
      <ul class="list-disc ml-4 text-gray-600">
        <li v-for="(item, index) in items" :key="index" class="flex items-center font-normal text-[19px]">
          
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
  
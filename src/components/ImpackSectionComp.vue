<template>
    <div class="md:flex justify-evenly items-center leading-12">
      <div class="mx-4">
        <div class="inline-block w-[100px] h-[100px] mx-auto flex items-center justify-center bg-gray-200 rounded-full">
          <slot name="icon"></slot>
        </div>
      </div>
      <div class="text-center md:text-left">
        <h3 class="text-xl font-semibold">{{ title }}</h3>
        <p class="text-gray-600 mt-2 line-clamp-3">
          {{ description }}
        </p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true,
      },
      description: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
 
  </style>
  
<template>
    <div class="md:flex justify-evenly items-center leading-12">
      <div class="mx-4">
        <div class="inline-block w-[88px] h-[88px] md:w-[100px] md:h-[100px] mx-auto flex items-center justify-center bg-gray-200 rounded-full">
          <slot name="icon"></slot>
        </div>
      </div>
      <div class="text-center md:text-left font-poppins">
        <h3 class="text-[28px] md:text-[32px] font-poppins pb-[15px] font-semibold">{{ title }}</h3>
        <p class="text-[18px] md:text-[22px] font-normal ">
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
  
<template>
    <header class="shadow-b-2xl bg-white border-b font-poppins">
      <nav class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class=" ">
             <img class="w-[84px] h-[35px] md:h-[92px] md:w-[250px] " src="../assets/Infiniwave-logo.png" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <Bars3Icon class="h-[20px] w-[40px]" aria-hidden="true" />
          </button>
        </div>
        <PopoverGroup class="hidden lg:flex font-normal text-[21px] items-center leading-[31px] lg:gap-x-12">
          <a href="" class="text-sm/6 font-semibold text-gray-900">Accueil</a>                    
          <a href="#" class="text-sm/6 font-semibold text-gray-900">À propos</a>
          <a href="#" class="text-sm/6 font-semibold text-gray-900">Projets</a>      
          <a href="" class="text-sm/6 font-semibold text-gray-900" >Services</a> 
          <a href="#" class="text-sm/6 font-semibold text-gray-900">Contact</a>                    
        </PopoverGroup>
        <NavFootBTn />

      </nav>
          
     
      <Dialog class="lg:hidden w-full" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
             <div class="fixed inset-0 z-10" />
        <DialogPanel class="fixed text-center inset-y-0 right-0 z-10 flex w-full flex-col justify-center items-center overflow-y-auto bg-white sm:max-w-full sm:ring-1 sm:ring-gray-900/10">
           <div class="p-6 mx-auto w-full flex flex-col items-center">
              <div class="flex flex-col items-center justify-center">
                <button type="button" class="-m-2.5 rounded-md pt-9 my-4 text-black" @click="mobileMenuOpen = false">
                  <XMarkIcon class="h-[20px] w-[40px] font-bold" aria-hidden="true" />
                </button>
                <a href="#" class="-m-1.5  text-center">
                 <img class="h-[51px] w-[123px]" src="../assets/Infiniwave-logo.png" alt="" />
                </a>
             </div>

            <div class="mt-6 w-full">
              <div class="flex flex-col items-center space-y-2 py-[34px]">
                <a v-for="item in products" :key="item.name" :href="item.href" class="group flex items-center gap-x-6 rounded-lg p-2 text-base font-semibold text-center">
                 {{ item.name }}
                </a>
              </div>
         
             <div class="py-4">
               <a href="#" class="h-[51px] w-[123px] font-semibold text-white rounded-lg px-4 py-1 bg-[#003049]">Réserver un appel</a>
             </div>
           </div>
       </div>
      </DialogPanel>
    </Dialog>
   </header>
 </template>
  
  <script setup>
  import NavFootBTn from './NavFootBTn.vue';
  import { ref } from 'vue'
  import {
    Bars3Icon,
    XMarkIcon,
  } from '@heroicons/vue/24/outline'

  
  const products = [
    { name: 'Accueil' },
    { name: 'À propos' },
    { name: 'Projets' },
    { name: 'Services' },
    { name: 'Contact' },
  ]


  const mobileMenuOpen = ref(false)
  </script>
<template>
    <header class=" shadow-xl bg-white border-b">
      <nav class="mx-auto flex max-w-7xl items-center justify-between p-6 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
             <img class="h-8 w-auto" src="../assets/Infiniwave-logo.png" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <PopoverGroup class="hidden lg:flex lg:gap-x-12">
          <a href="" class="text-sm/6 font-semibold text-gray-900">Accueil</a>                    
          <a href="#" class="text-sm/6 font-semibold text-gray-900">À propos</a>
          <a href="#" class="text-sm/6 font-semibold text-gray-900">Projets</a>      
          <a href="" class="text-sm/6 font-semibold text-gray-900" >Services</a> 
          <a href="#" class="text-sm/6 font-semibold text-gray-900">Contact</a>                    
        </PopoverGroup>
        <div class="hidden lg:flex lg:flex-1 lg:justify-end">
          <a href="#" class="text-sm/6 font-semibold text-white rounded-lg px-4 bg-[#003049]">Réserver un appel</a>
        </div>
      </nav>
                    <!-- below here ... check it up -->
      <Dialog class="lg:hidden mx-auto w-full" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-10" />
        <DialogPanel class="fixed text-center inset-y-0 right-0 z-10 flex w-full flex-col justify-between overflow-y-auto bg-white sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="p-6">

            <div class="flex items-center justify-between">
              <a href="#" class="-m-1.5 p-1.5 text-center">
                 <img class="h-8 w-auto" src="../assets/Infiniwave-logo.png" alt="" />
              </a>
              <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
                 <XMarkIcon class="h-6 w-6" aria-hidden="true" />
              </button>
            </div>

            <div class="mt-6 flow-root">
              <div class="-my-6 divide-y divide-gray-500/10">
                <div class="space-y-2 py-6">
                  <a v-for="item in products" :key="item.name" :href="item.href" class="group -mx-3 flex items-center gap-x-6 rounded-lg p-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">
                    <div class="flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                      <component :is="item.icon" class="h-6 w-6 text-gray-600 group-hover:text-indigo-600" aria-hidden="true" />
                    </div>
                    {{ item.name }}
                  </a>
                </div>
                <div class="py-6  ">
                  <a href="#" class="text-sm/6 font-semibold text-white rounded-lg px-4 py-1 bg-[#003049]">Réserver un appel</a>
                </div>
              </div>
            </div>

          </div>

          <div class="sticky bottom-0 grid grid-cols-2 divide-x divide-gray-900/5 bg-gray-50 text-center">
            <a v-for="item in callsToAction" :key="item.name" :href="item.href" class="p-3 text-base/7 font-semibold text-gray-900 hover:bg-gray-100">{{ item.name }}</a>
          </div>

        </DialogPanel>
      </Dialog>
    </header>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import {
    Bars3Icon,
    XMarkIcon,
  } from '@heroicons/vue/24/outline'
  import { PhoneIcon, PlayCircleIcon } from '@heroicons/vue/20/solid'
  
  const products = [
    { name: 'Accueil' },
    { name: 'À propos' },
    { name: 'Projets' },
    { name: 'Services' },
    { name: 'Contact' },
  ]
  const callsToAction = [
    { name: 'Watch demo', href: '#', icon: PlayCircleIcon },
    { name: 'Contact sales', href: '#', icon: PhoneIcon },
  ]

  const mobileMenuOpen = ref(false)
  </script>
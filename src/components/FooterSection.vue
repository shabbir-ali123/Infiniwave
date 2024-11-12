<template>
     <footer class="py-4 px-4 dark:text-white text-black font-poppins bg-[#fffff]">
        <div class="container mx-auto max-w-5xl border-b rounded pb-4">
          <div class="flex flex-col md:flex-row md:justify-between items-center text-left space-y-4 sm:space-y-0 ">
            <div class="w-[170px] h-[51px] mr-auto md:mr-0">
              <img :src="require('@/assets/Infiniwave-logo.png')" alt="Description">
            </div>
            <ul class="text-left mr-auto md:m-0 md:flex md:space-x-8 text-black space-y-6 py-8 md:space-y-0">
              <li>Accueil</li>
              <li>À propos</li>
              <li>Projets</li>
              <li>Services</li>
              <li>Contact</li>
            </ul>
            <div class="flex mr-auto md:m-0 space-x-4  ">
              <img :src="require('@/assets/linkedin/Outline.png')" class="w-[44px] h-[42px]" alt="Description">
              <img :src="require('@/assets/whatsapp/Outline.png')" class="w-[44px] h-[42px]" alt="Description">
            </div>
          </div>
        </div>
       

              
<div class="container d-block md:flex md:justify-between mx-auto md:text-center py-8 px-4 max-w-5xl">
  <p class="w-full md:w-auto">© Infiniwave 2023, Tous droits réservés</p>
  <p class="w-full md:w-auto mt-4 md:mt-0">Politique de confidentialité</p>
</div>

    </footer>
  </template>
  
  <script>
  export default {};
  </script>
  
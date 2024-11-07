<template>
     <footer class="py-4 px-4 dark:text-white text-black ">
        <div class="container mx-auto max-w-5xl border-b rounded">
          <div class="flex flex-col md:flex-row justify-between items-center space-y-4 sm:space-y-0 text-center sm:text-left py-4 px-4">
            <div class="w-[170px] h-[51px]">
              <img :src="require('@/assets/Infiniwave-logo.png')" alt="Description">
            </div>
            <ul class="flex space-x-8 text-black mt-4 ">
              <li>Accueil</li>
              <li>À propos</li>
              <li>Projets</li>
              <li>Services</li>
              <li>Contact</li>
            </ul>
            <div class="flex space-x-4 ">
              <img :src="require('@/assets/linkedin/Outline.png')" class="w-[44px] h-[42px]" alt="Description">
              <img :src="require('@/assets/whatsapp/Outline.png')" class="w-[44px] h-[42px]" alt="Description">
            </div>
          </div>
        </div>
                   <!-- Last footer side is here -->
      <div class="container flex justify-between mx-auto text-center py-8 px-4 max-w-5xl">
        <p>© Infiniwave 2023, Tous droits réservés</p>
        <p class="">Politique de confidentialité</p>
      </div>
    </footer>
  </template>
  
  <script>
  export default {};
  </script>
  
<template>
  <div class="font-poppins" style="background-image: linear-gradient(to bottom, #ffffff 0%, #99E2B4 50%, #ffffff 100%);">
    <div class="mx-auto max-w-7xl px-6 py-24 sm:py-32 lg:px-8 ">
      <div class="mx-auto max-w-4xl divide-y divide-gray-900/10">
        <h2 class="md:text-[68px] font-semibold text-center text-[38px]">Questions les plus posées</h2>
        <dl class="mt-10 space-y-4 divide-y divide-gray-900/10">
          <Disclosure as="div" v-for="faq in faqs" :key="faq.question" class="" v-slot="{ open }">
            <dt>
              <DisclosureButton class="flex w-full bg-white items-start justify-between text-left text-black  px-[16px] py-[14px]">
                <span class="text-base/7 font-semibold font-[28px] font-medium">{{ faq.question }}</span>
                <span class="ml-6 flex h-7 items-center ">
                  <ChevronDownIcon v-if="!open" class="h-6 w-6" aria-hidden="true" />
                  <ChevronUpIcon v-else class="h-6 w-6" aria-hidden="true" />
                </span>
              </DisclosureButton>
            </dt>
            <DisclosurePanel as="dd" class="px-[45px] py-[16px] bg-[#EAE0D5]">
              <p class="text-base/7 text-gray-600">{{ faq.answer }}</p>
            </DisclosurePanel>
          </Disclosure>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue'
import { ChevronUpIcon, ChevronDownIcon } from '@heroicons/vue/24/outline'

const faqs = [
  {
    question: "Quels sont les tarifs pour vos services ?",
    answer:
      "I don't know, but the flag is a big plus. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas cupiditate laboriosam fugiat.",
  },
  {
    question: "Quels sont les tarifs pour vos services ?",
    answer:
      "Nos tarifs sont ajustés en fonction de vos besoins spécifiques. Ils varient selon le nombre de pages, les fonctionnalités à intégrer et la complexité du projet. N'hésitez pas à nous contacter pour en discuter davantage.",
  },
  {
    question: "Combien de temps un projet de site web prend-t-il ?",
    answer:
      "Not available .",
  },
  {
    question: "Combien de temps un projet de site web prend-t-il ?",
    answer:
      "Un site web standard de 5 à 10 pages peut être réalisé en environ 3 semaines. Ce délai peut varier en fonction de la complexité du projet. Nous nous engageons à vous livrer un site de qualité dans des délais raisonnables.",
  },
  {
    question: "Pourquoi opter pour un site éco-responsable et accessible ?",
    answer:
      "Not available .",
  },
  {
    question: "Pourquoi opter pour un site éco-responsable et accessible ?",
    answer:
      "Choisir un site éco-responsable et accessible, c’est réduire votre empreinte carbone tout en garantissant que tous les utilisateurs, y compris ceux en situation de handicap, puissent naviguer facilement. Cela élargit votre audience et démontre votre engagement envers des valeurs durables et inclusives. C'est un investissement judicieux pour votre image et pour la planète.",
  },
 ]
</script>
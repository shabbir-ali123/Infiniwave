<!-- src/components/ImpactSectionsParent.vue -->

<template>
  <section
    class="font-poppins"
    style="background-image: linear-gradient(to bottom, #ffffff 0%, #99E2B4 50%, #ffffff 100%);"
  >
    <h2
      class="text-center text-[28px] md:text-[68px] font-semibold pt-[42px] md:pt-[70px] pb-[52px] md:pb-[123px]"
    >
      Transformez votre impact digital
    </h2>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8 px-4 lg:gap-8">
      <ImpactSectionComp
        v-for="(section, index) in impactSections"
        :key="index"
        :title="section.title"
        :description="section.description"
      >
        <template #icon>
          <component :is="section.icon" />
        </template>
      </ImpactSectionComp>
    </div>
  </section>
</template>

<script>
import ImpactSectionComp from './ImpactSectionComp.vue';
import EcologicalImpactIcon from '../assets/svgs/EcologicalImpactIcon.vue';
import VisibilityBoostIcon from '../assets/svgs/VisibilityBoostIcon.vue';
import AccessibilityIcon from '../assets/svgs/AccessibilityIcon.vue';
import CompetitionIcon from '../assets/svgs/CompetitionIcon.vue';

export default {
  name: 'ImpactSectionsParent',
  components: {
    ImpactSectionComp,
    EcologicalImpactIcon,
    VisibilityBoostIcon,
    AccessibilityIcon,
    CompetitionIcon,
  },
  data() {
    return {
      impactSections: [
        {
          title: 'Réduisez votre impact écologique',
          description:
            'Un site optimisé qui consomme moins de ressources, pour un impact environnemental réduit et des performances maximisées.',
          icon: EcologicalImpactIcon,
        },
        {
          title: 'Boostez votre visibilité en ligne',
          description:
            'Profitez d’un site rapide et intuitif qui améliore l’expérience utilisateur et renforce votre référencement naturel.',
          icon: VisibilityBoostIcon,
        },
        {
          title: 'Rendez votre site accessible à tous',
          description:
            'Un site conçu pour être utilisé par tous, élargissant votre audience et répondant aux normes d’inclusivité.',
          icon: AccessibilityIcon,
        },
        {
          title: 'Démarquez-vous de la concurrence',
          description:
            'Avec un site unique, éco-conçu et accessible, vous offrez une expérience que vos concurrents n’égalent pas. Soyez la référence en combinant performance et innovation.',
          icon: CompetitionIcon,
        },
      ],
    };
  },
};
</script>

<style scoped>
/* Add any scoped styling if needed */
</style>

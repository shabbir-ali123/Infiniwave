<!-- src/components/CardDataParent.vue -->
<template>
  <section
    class="font-poppins"
    style="background-image: linear-gradient(to bottom, #ffffff 0%, #99E2B4 50%, #ffffff 100%);"
  >
    <h2 class="text-center text-[28px] md:text-[68px] font-semibold py-[72px] md:py-[100px]">
      3 Phases Pour Élever Votre Présence <br /> Digitale
    </h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 px-8 lg:px-12">
      <CardData
        v-for="(card, index) in cards"
        :key="index"
        :title="card.title"
        :items="card.items"
      >
        <template #icon>
          <component :is="card.icon" />
        </template>
      </CardData>
    </div>
  </section>
</template>

<script>
import CardData from './CardData.vue';
import DesignIcon from '../assets/svgs/DesignIcon.vue';
import CreationIcon from '../assets/svgs/CreationIcon.vue';
import DeploymentIcon from '../assets/svgs/DeploymentIcon.vue';

export default {
  name: 'CardDataParent',
  components: {
    CardData,
    DesignIcon,
    CreationIcon,
    DeploymentIcon,
  },
  data() {
    return {
      cards: [
        {
          title: 'Design',
          items: [
            'Maquette sur mesure',
            'Personnalisation illimitée',
            'Solution évolutive',
            'Design impactant',
            'Validation avant le développement',
            'Expérience utilisateur fluide',
            'Image de marque renforcée',
          ],
          icon: DesignIcon,
        },
        {
          title: 'Création',
          items: [
            'Code optimisé et léger',
            'Conception éco-responsable',
            'Site accessible',
            'Conception responsive',
            'Gestion de la maintenance',
            'Optimisation des performances',
            'Contenu dynamique (si demandé)',
            
          ],
          icon: CreationIcon,
        },
        {
          title: 'Déploiement',
          items: [
            'Déploiement rapide',
            'Optimisation automatique',
            'Sécurité renforcée',
            'Sauvegardes automatiques',
            'Mises à jour simplifiées',
            'Chargement rapide',
            'Maintenance prise en charge',
          ],
          icon: DeploymentIcon,
        },
        // If you have a fourth card, add it here
        // {
        //   title: 'Another Phase',
        //   items: [...],
        //   icon: AnotherIcon,
        // },
      ],
    };
  },
};
</script>

<style scoped>
/* Add any scoped styling if needed */
</style>

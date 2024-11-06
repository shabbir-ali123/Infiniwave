<template>
  <div>
    <HeroSection />
    <WhyEco />
    <ImpactSection />
    <PhasesSection />
    <FAQSection />
    <Footer />
  </div>
</template>

<script>
import HeroSection from './components/HeroSection.vue';
import WhyEco from './components/WhyEco.vue';
import ImpactSection from './components/ImpactSection.vue';
import PhasesSection from './components/PhasesSection.vue';
import FAQSection from './components/FAQSection.vue';
import Footer from './components/FooterSection.vue';

export default {
  components: {
    HeroSection,
    WhyEco,
    ImpactSection,
    PhasesSection,
    FAQSection,
    Footer,
  },
};
</script>

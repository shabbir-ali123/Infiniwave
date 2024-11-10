<template>
  <div>
    <HeaderSection />
    <HeroSection />
    <WhyEco />
    <ImpactSection />
    <PhasesSection />
    <FAQSection />
    <Footer />
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue';
import HeroSection from './components/HeroSection.vue';
import WhyEco from './components/WhyEco.vue';
import ImpactSection from './components/ImpactSection.vue';
import PhasesSection from './components/PhasesSection.vue';
import FAQSection from './components/FAQSection.vue';
import Footer from './components/FooterSection.vue';



export default {
  components: {
    HeaderSection,
    HeroSection,
    WhyEco,
    ImpactSection,
    PhasesSection,
    FAQSection,
    Footer,
  },
};
</script>

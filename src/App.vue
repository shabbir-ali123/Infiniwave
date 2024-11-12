<template>
  <div>
    <HeaderSection />
    <HeroSection />
    <WhyEco />
    <div style=' 
      background-image: radial-gradient(circle, #99E2B4,#f9f9f9)'>
    <ImpactSection />
    <PhasesSection />
    <FAQSection />
    </div>
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

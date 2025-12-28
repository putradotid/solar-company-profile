<template>
  <div>
    <Hero />
    <InfoSection />
    <HeroImage image="https://digitalassets.tesla.com/tesla-contents/image/upload/f_auto,q_auto/price-solar-desktop" />
    <FeatureSection />
    <HeroImage image="https://digitalassets.tesla.com/image/upload/q_auto/f_auto/w_1920/prod/fulfillment/energy/Order/VirtualConsultations/VC_d_v2" />
  </div>
</template>

<script setup>
import Hero from '../components/Hero.vue'
import InfoSection from '../components/InfoSection.vue'
import FeatureSection from '../components/FeatureSection.vue'
import HeroImage from '../components/HeroImage.vue'
</script>

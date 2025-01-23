<script setup>
import Features from '~/components/landing/Features.vue';
import Gallery from '~/components/landing/Gallery.vue';

definePageMeta({
  layout: "landing",
});
</script>

<template>
  <LandingContainer>
    <LandingHero></LandingHero>
    <!-- <LandingFeatures></LandingFeatures> -->
    <Gallery></Gallery>
    <LandingLogos></LandingLogos>
    <LandingCta></LandingCta>
  </LandingContainer>
</template>

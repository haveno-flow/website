<template>
  <div class="bg-white">
    <main class="isolate">
      <!-- Hero section + Logo cloud fill the viewport -->
      <div class="min-h-screen">
        <!-- Header sits absolute over the hero -->
        <AppHeader />
        <HeroSection />
        <LogoCloud />
      </div>

      <!-- Feature section -->
      <FeatureSection />

      <!-- FAQ section -->
      <FaqSection />

    </main>

    <!-- Footer -->
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import LogoCloud from './components/LogoCloud.vue'
import FeatureSection from './components/FeatureSection.vue'
import FaqSection from './components/FaqSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>

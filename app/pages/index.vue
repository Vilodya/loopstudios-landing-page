<script setup lang="ts">
import Header from '~/components/layout/Header.vue';
import InteractiveSection from '~/components/sections/InteractiveSection.vue';
import CreationsSection from '~/components/sections/CreationsSection.vue';
import HeroSection from '~/components/sections/HeroSection.vue';
import Footer from '~/components/layout/Footer.vue';
</script>

<template>
  <div>
    <Header />
    <main>
      <HeroSection />
      <InteractiveSection />
      <CreationsSection />
    </main>
    <Footer />
  </div>
</template>

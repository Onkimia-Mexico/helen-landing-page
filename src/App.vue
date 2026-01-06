<script setup>
/* --------------------------------------------------
   Root Application Layout
   --------------------------------------------------
   Purpose:
   - Compose the main landing page structure
   - Import and render all top-level sections
   - Define anchor targets for navigation
   -------------------------------------------------- */

import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import About from './components/About.vue'
import FeatureSection from './components/FeatureSection.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <!-- Global header (fixed navigation) -->
  <Header />

  <!-- Hero / Entry point -->
  <section id="inicio">
    <HeroSection />
  </section>

  <!-- About / Value proposition -->
  <section id="nosotros">
    <About />
  </section>

  <!-- Features / Services -->
  <section id="servicios">
    <FeatureSection />
  </section>

  <!-- Contact / Lead capture -->
  <section id="contacto">
    <Contact />
  </section>

  <!-- Global footer -->
  <Footer />
</template>

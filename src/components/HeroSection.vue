<script setup>
/* --------------------------------------------------
 * HeroSection.vue
 * --------------------------------------------------
 * Purpose:
 * - Present the main value proposition
 * - Showcase platform UI with an infinite vertical carousel
 * - Add subtle parallax motion to the decorative background
 * -------------------------------------------------- */

import { ref, onMounted, onUnmounted } from 'vue'

/* ---------------- Assets ---------------- */
/* Platform mockups used in the carousel */
import mockLogin from '../assets/mockup login.webp'
import mockClinical from '../assets/mockup exp clin.webp'
import mockCalendar from '../assets/mockup salas.webp'

/* ---------------- Carousel Data ---------------- */
/* Base mockup list */
const mockups = [
  { src: mockLogin },
  { src: mockClinical },
  { src: mockCalendar}
]

/* Duplicated list to allow seamless infinite scrolling */
const mockupsDuplicated = [...mockups, ...mockups]

/* ---------------- Parallax Logic ---------------- */
/* Reference to the decorative background image */
const heroBg = ref(null)

/* Scroll handler for vertical parallax effect */
const onScroll = () => {
  if (!heroBg.value) return
  heroBg.value.style.transform = `translateY(${window.scrollY * 0.35}px)`
}

/* Lifecycle hooks */
onMounted(() => {
  window.addEventListener('scroll', onScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', onScroll)
})
</script>

<template>
  <section class="hero">

    <!-- Decorative parallax background -->
    <img
      ref="heroBg"
      src="../assets/background.webp"
      alt=""
      class="hero-bg"
      aria-hidden="true"
    />

    <div class="hero-container">

      <!-- Left column: headline and call to action -->
      <div class="hero-left">
        <h1>La plataforma clínica que conecta atención médica, operación y control.</h1>
        <p>
          Desde el expediente clínico hasta el control administrativo: 
          <strong>centralizamos toda tu operación</strong> en un entorno intuitivo, trazable y seguro.
        </p>
        <div class="hero-actions">

          <a href="#contacto" class="btn-primary">
            Agendar demo
          </a>

          <a href="#nosotros" class="btn-secondary">
            Conócenos
          </a>
        </div>
      </div>

      <!-- Right column: vertical auto-scrolling mockup carousel -->
      <div class="hero-right">
        <div class="vertical-slider">
          <div class="vertical-track">
            <img 
              v-for="(mock, index) in mockupsDuplicated" 
              :key="index" 
              :src="mock.src" 
              class="v-mockup" 
              alt="Interfaz Helen MS"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>






<template>
  <!-- --------------------------------------------------
       Header / Main Navigation
       --------------------------------------------------
       Purpose:
       - Display brand identity
       - Provide primary site navigation
       - Remains fixed at the top of the viewport
       -------------------------------------------------- -->
  <header class="header">

    <!-- Brand / Logo -->
    <div class="brand">
      <img
        src="../assets/logo.webp"
        alt="Helen MS logo"
      />
      <span class="brand-text">Helen MS</span>
    </div>

    <!-- Primary navigation -->
    <nav class="nav">
      <a href="#inicio">Inicio</a>
      <a href="#nosotros">Nosotros</a>
      <a href="#servicios">Servicios</a>
      <a href="#contacto">Contacto</a>
      <a href="#contacto">Agendar demo</a>
    </nav>

    <!-- Hamburger -->
    <button
      class="hamburger"
      @click="menuOpen = !menuOpen"
      aria-label="Toggle menu"
    >
      <span :class="{ open: menuOpen }"></span>
      <span :class="{ open: menuOpen }"></span>
      <span :class="{ open: menuOpen }"></span>
    </button>
  </header>
  
  <!-- Mobile menu -->
  <div class="mobile-menu" v-if="menuOpen">
    <a href="#nosotros" @click="menuOpen = false">Nosotros</a>
    <a href="#servicios" @click="menuOpen = false">Servicios</a>
    <a href="#contacto" @click="menuOpen = false">Contacto</a>
  </div>
</template>

<script setup>

import { ref } from 'vue'
const menuOpen = ref(false)

</script>


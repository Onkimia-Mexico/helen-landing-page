<script setup>
/* --------------------------------------------------
 * About.vue
 * --------------------------------------------------
 * Purpose:
 * - Explain why Helen MS is different
 * - Highlight key product differentiators
 * - Reinforce credibility through client logos
 * -------------------------------------------------- */

/* ---------------- Assets ---------------- */
/* Client logos used in the infinite carousel */
import logoOnkimia from '../assets/onkimia-logo.webp'
import logoICAN from '../assets/LOGO-ICAN.webp'
import logoEndos from '../assets/endos.webp'
import logoCuidare from '../assets/cuidare.webp'

/* ---------------- Carousel Data ---------------- */
/* Base logo list */
const logos = [
  { src: logoOnkimia, big: false },
  { src: logoICAN, big: true },
  { src: logoEndos, big: true },
  { src: logoCuidare, big: true }
]

/* Duplicated list for seamless infinite scrolling */
const logosDuplicated = [...logos, ...logos]
</script>


<template>
  <section class="about">
    <div class="about-inner">

      <!-- Visual slogan / supporting illustration -->
      <img
        src="../assets/slogan.webp"
        alt="Slogan Helen MS"
        class="about-slogan"
      />
    
     <!-- Textual content -->
      <div class="about-content">
        <h2>¿Por qué elegir Helen MS?</h2>
      
        <!-- Key differentiators list -->
        <ul class="icon-bullets">
          <li>
            <i class="fi fi-rr-user-md-chat"></i>
            <span><strong>Experiencia Real:</strong> Diseñado por médicos, para médicos.</span>
          </li>
          <li>
            <i class="fi fi-rr-ribbon"></i>
            <span><strong>Alta Complejidad:</strong> Especializados en oncología y entornos de alta precisión.</span>
          </li>
          <li>
            <i class="fi fi-rr-master-plan-integrate"></i>
            <span><strong>Integración Total:</strong> Tu expediente clínico y el ERP en un solo lugar.</span>
          </li>
          <li>
            <i class="fi fi-rr-calendar-shift-swap"></i>
            <span><strong>Versatilidad:</strong> Flexible y adaptable a cualquier especialidad médica.</span>
          </li>
          <li>
            <i class="fi fi-rs-shield-check"></i>
            <span><strong>Seguridad:</strong> Datos encriptados y respaldados automáticamente en la nube.</span>
          </li>
          <li>
            <i class="fi fi-rr-data-migration"></i>
            <span><strong>Migración sin dolor:</strong> Nosotros exportamos tus datos actuales al sistema.</span>
          </li>
          <li>
            <i class="fi fi-rr-devices"></i>
            <span><strong>Movilidad Total:</strong> Acceso seguro desde cualquier dispositivo.</span>
          </li>
        </ul>

      </div>
    </div>

    <!-- Client logos carousel -->
    <div class="clients-slider">
      <div class="slider-track">
        <img 
          v-for="(logo, index) in logosDuplicated" 
          :key="index" 
          :src="logo.src" 
          :alt="'Cliente ' + (index+1)"
          :class="{ 'big-logo': logo.big }"
          />
      </div>
    </div>

  </section>
</template>


<script setup>
/* --------------------------------------------------
 * Contact.vue
 * --------------------------------------------------
 * Purpose:
 * - Display a contact form
 * - Send lead information via EmailJS
 * - Apply a parallax background effect while visible
 * -------------------------------------------------- */

import { ref, onMounted, onUnmounted } from 'vue'
import emailjs from '@emailjs/browser'

/* ---------------- EmailJS Configuration ----------------
 * These values come directly from EmailJS dashboard
 * (Service ID, Template ID and Public Key)
 */
const SERVICE_ID = 'service_es3rii9'
const TEMPLATE_ID = 'template_zjlbgz1'
const PUBLIC_KEY = '9YTWZ1y32lja31xmA'

/* ---------------- Refs ---------------- */
/* Contact form reference (used by EmailJS) */
const form = ref(null)

/* Parallax background */
const contactBg = ref(null)

/* Section root element (visibility detection) */
const contactSection = ref(null)

/* UI states */
const loading = ref(false)
const success = ref(false)
const error = ref(false)

/* ---------------- Email Logic ---------------- */
/**
 * Sends the contact form data using EmailJS
 */
const sendEmail = async () => {
  loading.value = true
  success.value = false
  error.value = false

  try {
    await emailjs.sendForm(
      SERVICE_ID,
      TEMPLATE_ID,
      form.value,
      PUBLIC_KEY
    )

    success.value = true
    form.value.reset()
  } catch (err) {
    console.error('EmailJS error:', err)
    error.value = true
  } finally {
    loading.value = false
  }
}

/* ---------------- Parallax Logic ---------------- */
/**
 * Applies a vertical parallax translation to the
 * background image while the section is visible
 */
const onScroll = () => {
  if (!contactBg.value || !contactSection.value) return

  const rect = contactSection.value.getBoundingClientRect()
  const windowHeight = window.innerHeight

  if (rect.top < windowHeight && rect.bottom > 0) {
    const progress = Math.min(
      Math.max((windowHeight - rect.top) / (windowHeight + rect.height), 0),
      1
    )

    const eased = 1 - Math.pow(1 - progress, 2)
    contactBg.value.style.transform = `translateY(${eased * 120}px)`
  }
}

/* ---------------- Lifecycle ---------------- */
onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<template>
  <section class="contact" ref="contactSection">

    <!-- Decorative parallax background -->
    <img
      ref="contactBg"
      src="../assets/background.webp"
      class="contact-bg"
      alt=""
      aria-hidden="true"
      loading="lazy"
    />

    <div class="contact-wrapper">
      <div class="contact-info">
        <h2>Contacto</h2>
        <p>
          ¿Tienes dudas o quieres saber más sobre Helen MS? <br />
          Escríbenos y nos pondremos en contacto contigo.
        </p>
      </div>

      <!-- Contact form -->
      <form
        ref="form"
        class="contact-form"
        @submit.prevent="sendEmail"
      >
        <input
          type="text"
          name="name"
          placeholder="Nombre"
          required
        />

        <input
          type="email"
          name="email"
          placeholder="Correo electrónico"
          required
        />

        <textarea
          name="message"
          placeholder="Mensaje"
          required
        ></textarea>

        <button type="submit" :disabled="loading">
          {{ loading ? 'Enviando...' : 'Enviar mensaje' }}
        </button>

        <!-- Feedback messages -->
        <p v-if="success" class="success-msg">
          Mensaje enviado correctamente, un asesor se pondrá en contacto con usted.
        </p>

        <p v-if="error" class="error-msg">
          Ocurrió un error. Inténtalo nuevamente.
        </p>
      </form>
    </div>
  </section>
</template>



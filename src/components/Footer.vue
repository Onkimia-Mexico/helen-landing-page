<template>
  <!-- --------------------------------------------------
       Footer
       --------------------------------------------------
       Purpose:
       - Display brand identity
       - Provide navigation links
       - Show social media and contact information
       -------------------------------------------------- -->
  <footer class="footer">
    <div class="footer-content">

      <!-- Brand / Logo -->
      <div class="footer-col footer-logo">
        <img
          src="../assets/Logotipo2.png"
          alt="Helen MS"
          class="footer-info"
        />
      </div>

      <!-- Navigation menu -->
      <div class="footer-col footer-menu">
        <h4>Menú</h4>
        <ul class="footer-list">
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#servicios">Servicios</a></li>
          <li><a href="#nosotros">Nosotros</a></li>
          <li><a href="#contacto">Contacto</a></li>
        </ul>
      </div>

      <!-- Social media links -->
      <div class="footer-col footer-menu">
        <h4>Redes</h4>
        <ul class="footer-list footer-social">
          <li>
            <a href="#">
              <i class="fi fi-brands-linkedin"></i>
              LinkedIn
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fi fi-brands-facebook"></i>
              Facebook
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fi fi-brands-instagram"></i>
              Instagram
            </a>
          </li>
        </ul>
      </div>

      <!-- Contact information -->
      <div class="footer-col footer-contact">
        <h4>Contacto</h4>

        <ul class="footer-list footer-contact-list">
          <li>
            <a href="mailto:contacto@helenms.com">
              <i class="fi fi-sr-envelope"></i>
              <span>contacto@helenms.com</span>
            </a>
          </li>

          <li>
            <i class="fi fi-sr-phone-call"></i>
            <span>+52 33 3496 4995</span>
          </li>

          <li>
            <i class="fi fi-sr-marker"></i>
            <span>
              C. Beethoven 287, Juan Manuel,<br />
              44680 Guadalajara, Jal.
            </span>
          </li>
          
          <!--
          <li>
            <i class="fi fi-ss-customer-service"></i>
            <span>+52 33 0000 0000</span>
          </li> -->
        </ul>
      </div>

    </div>

    <!-- Copyright -->
    <div class="footer-bottom">
      © {{ new Date().getFullYear() }} Helen. Todos los derechos reservados.
    </div>
  </footer>
</template>

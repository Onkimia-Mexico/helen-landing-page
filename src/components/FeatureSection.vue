<template>
  <section class="features">
    <div class="features-header">
      <h2>Nuestros servicios en una sola solución</h2>
      <p>Todo lo que necesitas para tu operación, en un solo lugar.</p>
    </div>

    <div class="features-grid">

<!------------------- EXPEDIENTE CLÍNICO --------------------->

      <div class="feature-clinical-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rs-patient-file"></i>
            </div>
            <h3>Expediente clínico electrónico</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Registro del historial clínico del paciente,
              con trazabilidad, seguridad y acceso inmediato.</li>
              <li>Conforme NOM-004-SSA3-2012 y NOM-024-SSA3-2012.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>

        </div>
      </div>

<!------------------- AGENDA DE CONSULTAS --------------------->

      <div class="feature-clinical-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rs-address-book"></i>
            </div>
            <h3>Agenda de consultas médicas</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Vista calendario con filtros por estado (Aprobada, rechazada, pendiente).</li>
              <li>Recordatorios automatizados.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>

        </div>
      </div>

<!------------------- NOTAS CLÍNICAS --------------------->
      
      <div class="feature-clinical-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rr-user-md"></i>
            </div>
            <h3>Notas clínicas por especialidad</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Plantillas personalizadas para cada especialidad.</li>
              <li>Dictado por voz y carga rápida de documentos para optimizar el tiempo de consulta.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>

        </div>
      </div>

<!------------------- SALAS DE TRATAMIENTO --------------------->

      <div class="feature-clinical-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rs-hospital-bed"></i>
            </div>
            <h3>Gestión de salas de tratamiento</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Control del flujo de pacientes en áreas de quimioterapia o procedimientos.</li>
              <li>Vista de lista o calendario con filtros de estados.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>

        </div>
      </div>

<!------------------- VISUALIZACIÓN DE IMÁGENES --------------------->

      <div class="feature-clinical-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rr-x-ray"></i>
            </div>
            <h3>Visualización de imágenes médicas</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Integración con sistemas Nifti/DICOM para ver estudios directamente en el expediente.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>

        </div>
      </div>

<!------------------- ERP para clínicas --------------------->

      <div class="feature-ops-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rs-file-invoice-dollar"></i>
            </div>
            <h3>ERP para clínicas</h3>
            <img
              src="../assets/Odoo.png"
              alt="ERP para clínicas"
              class="feature-image"
            />
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Administración financiera integral: facturación electrónica, egresos y cuentas por cobrar.</li>
              <li>Reportes en tiempo real para la toma de decisiones.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>
        </div>
      </div>

<!------------------- Gestión de inventarios --------------------->

      <div class="feature-ops-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-rs-supplier-alt"></i>
            </div>
            <h3>Gestión de inventarios</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Control estricto de medicamentos (lotes y caducidades) e insumos médicos.</li>
              <li>Reabastecimiento automático de stock mínimo.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>
        </div>
      </div>

<!------------------- Whatsapp --------------------->

      <div class="feature-ops-card flip" role="button">
        <div class="flip-inner">

          <!-- FRONT -->
          <div class="flip-front">
            <div class="feature-icon">
              <i class="fi fi-brands-whatsapp"></i>
            </div>
            <h3>Whatsapp Bussines integrado al ERP</h3>
            <p class="hint">Click para saber más</p>
          </div>

          <!-- BACK -->
          <div class="flip-back">
            <ul class="bullets-features">
              <li>Envío automatizado de confirmaciones de cita y recordatorios directamente desde el ERP.</li>
            </ul>
            <p class="hint">Click para volver</p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  document.querySelectorAll('.flip').forEach(card => {
    const toggle = () => card.classList.toggle('is-flipped')
    card.addEventListener('click', toggle)
  })
})
</script>
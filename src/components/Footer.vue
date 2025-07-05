<script setup>
</script>

<template>
    <footer class="footer">
        <div class="contenidofooter">
            <p class="informacion-contacto">
                Contacto: <span class="email">oscarluquehidalgo@gmail.com</span>
            </p>
            <p class="derechos-de-autor">
                &copy; 2025 Óscar Luque Hidalgo
            </p>
        </div>
    </footer>
</template>

<style scoped>
/* =================================
   1. ESTILOS BASE (MÓVIL)
   ================================= */
.footer {
  background: #1a1a1a;
  color: #f4f4f4;
  /* El padding de móvil es ahora la base */
  padding: 30px 15px;
  text-align: center;
  border-top: 1px solid rgba(142, 253, 142, 0.2);
}

.contenidofooter {
  margin: 0 auto;
  display: flex;
  /* Por defecto, los elementos se apilan verticalmente */
  flex-direction: column;
  align-items: center;
  gap: 15px; /* Un poco más de separación vertical */
}

.derechos-de-autor {
  font-size: 0.9em;
  opacity: 0.8;
}

.email {
  color: #8efd8e;
  text-decoration: none;
  transition: color 0.3s ease;
}



@media (min-width: 768px) {
  .footer {
    padding: 25px 40px;
  }

  .contenidofooter {
    flex-direction: column;

    width: 100%;
    max-width: 1400px; 
  }
}
</style>
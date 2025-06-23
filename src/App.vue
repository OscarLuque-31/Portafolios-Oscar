<script setup>
import Cabecera from "./components/Cabecera.vue";
import Inicio from "./components/Inicio.vue";
import Experiencia from "./components/Experiencia.vue";
</script>

<template>
  <div class="contenido">
    <Cabecera></Cabecera>
    <Inicio></Inicio>
    <Experiencia></Experiencia>
  </div>
</template>

<style>
.contenido {
  background: linear-gradient(to bottom, #292828, #000000);
  background-repeat: no-repeat;
  background-size: cover;
}
</style>

<script setup>
import Cabecera from "./components/Cabecera.vue";
import Inicio from "./components/Inicio.vue";
import Experiencia from "./components/Experiencia.vue";
import Stack from "./components/Stack.vue";
</script>

<template>
  <div class="contenido">
    <Cabecera></Cabecera>
    <Inicio></Inicio>
    <Experiencia></Experiencia>
    <Stack></Stack>
  </div>
</template>

<style>
.contenido {
  background: linear-gradient(to bottom, #292828, #181C14);
  background-repeat: no-repeat;
  background-size: cover;
}
</style>

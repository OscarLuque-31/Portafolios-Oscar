<script setup>
import Cabecera from "./components/Cabecera.vue";
import Inicio from "./components/Inicio.vue";
import Experiencia from "./components/Experiencia.vue";
import Stack from "./components/Stack.vue";
import Proyectos from "./components/Proyectos.vue";
import Footer from "./components/Footer.vue";

</script>

<template>
  <div class="contenido">
    <Cabecera></Cabecera>
    <Inicio></Inicio>
    <Experiencia></Experiencia>
    <Proyectos></Proyectos>
    <Stack></Stack>
    <Footer></Footer>
  </div>
</template>

<style>
.contenido {
  background: linear-gradient(to bottom, #292828, #101110);
  background-repeat: no-repeat;
  background-size: cover;

  display: flex;
  flex-direction: column;
  gap: 100px;
}
</style>

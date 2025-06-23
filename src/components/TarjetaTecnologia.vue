<script setup>

const props = defineProps({
  imgUrl: String,
  backgroundColor: String
})

// Función para convertir hex a rgba
function hexToRgba(hex, opacity) {
  const r = parseInt(hex.slice(1, 3), 16)
  const g = parseInt(hex.slice(3, 5), 16)
  const b = parseInt(hex.slice(5, 7), 16)
  return `rgba(${r}, ${g}, ${b}, ${opacity})`
}

const bgColorWithOpacity = hexToRgba(props.backgroundColor, 0.1) // 0.2 = 20% de opacidad

</script>

<template>
  <div class="tarjeta" :style="{ boxShadow: `0 0 10px 3px ${backgroundColor}`, backgroundColor: bgColorWithOpacity }">
    <img :src="imgUrl" alt="Imagen de la tarjeta">
  </div>
</template>

<style>
.tarjeta {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 50px;
  padding: 8px;
  border-radius: 20px;
  margin-inline: 15px;
  transition: all 0.3s ease;
}

.tarjeta img {
  height: 35px;
}

.tarjeta:hover {
  transform: scale(1.1);
}

</style>

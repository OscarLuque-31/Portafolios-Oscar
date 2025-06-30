<script setup>

const props = defineProps({
  imgUrl: String,
  nombre: String,
  backgroundColor: String
})

// Función para convertir hex a rgba
function hexToRgba(hex, opacity) {
  const r = parseInt(hex.slice(1, 3), 16)
  const g = parseInt(hex.slice(3, 5), 16)
  const b = parseInt(hex.slice(5, 7), 16)
  return `rgba(${r}, ${g}, ${b}, ${opacity})`
}

console.log(`${props.imgUrl}`)

const bgColorWithOpacity = hexToRgba(props.backgroundColor, 0.1) // 0.2 = 20% de opacidad

</script>

<template>
  <div class="tarjeta" :style="{ boxShadow: `0 0 8px 1px ${backgroundColor}`, backgroundColor: bgColorWithOpacity }">
    <img :src="imgUrl" alt="Imagen de la tarjeta">
    <h2>{{ nombre }}</h2>
  </div>
</template>

<style scoped>
.tarjeta {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 40px;
  padding-inline: 15px;
  border-radius: 15px;
  transition: all 0.3s ease;
  gap: 15px;
}

.tarjeta img {
  height: 20px;
}

.tarjeta h2 {
    color: white;
    font-size: 15px;
    font-weight: 300;
}



</style>

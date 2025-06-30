<script setup>
import TarjetaTecnologiaProyecto from './TarjetaTecnologiaProyecto.vue';

defineProps({
    imgUrl: String,
    titulo: String,
    colorTitulo: String,
    enlaces: Array,
    subtitulo: String,
    tecnologias: Array
})

</script>

<template>
    <div class="proyecto">
        <div class="cabecera">
            <h2 :style="{ color: colorTitulo }">{{ titulo }}</h2>
            <div class="enlaces">
                <a v-for="enlace in enlaces" :key="enlace.id" :href="enlace.enlace" target="_blank"
                    rel="noopener noreferrer" class="svg-enlace" :style="{ color: colorTitulo }">
                    <div v-html="enlace.svg" :style="{ width: enlace.tamanyo }" />
                </a>
            </div>
        </div>
        <h3>{{ subtitulo }}</h3>
        <div class="tecnologias">
            <TarjetaTecnologiaProyecto v-for="(tecn, index) in tecnologias" :key="tecn.id || index"
                :nombre="tecn.nombre" :imgUrl="tecn.imgUrl" :backgroundColor="tecn.backgroundColor" />
        </div>
        <img :src="imgUrl" :alt="`Imagen de ${titulo}`">
    </div>
</template>

<style scoped>
.proyecto {
    max-width: 600px;
    border-radius: 10px;
    padding: 20px;

    color: white;
    transition: all 0.3s ease;
    padding: 10px;
    gap: 8px;
}

.proyecto img {
    max-width: 100%;
    height: auto;
    border-radius: 20px;
    margin-top: 20px;
}

.cabecera {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
}

.enlaces {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 20px;
}

.svg-enlace {
    display: flex;
    align-items: center;
    text-decoration: none;
}

.svg-enlace :deep(svg) {
    transition: transform 0.3s ease;
}

.svg-enlace:hover :deep(svg) {
    transform: scale(1.1);
}


.tecnologias {
    display: flex;
    flex-wrap: row;
    gap: 15px;
}


h2 {
    font-size: 28px;
    font-weight: 700;
}

h3 {
    font-size: 20px;
    line-height: 1.5;
    font-weight: 400;
    margin-top: 0px;
}

@media (max-width: 600px) {

    .proyecto {
        margin-inline: 20px;
    }

}
</style>

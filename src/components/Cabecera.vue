<script setup>
</script>

<template>
     <header class="cabecera">
        <nav>
            <a href="#presentacion">Inicio</a>
            <a href="#sobremi">Sobre mí</a>
            <a href="">Trayectoria</a>
            <a href="">Proyectos</a>
        </nav>
    </header>
</template>

<style scoped>
    .cabecera{
        display: flex;
        justify-content: space-around;
        align-items: center;
        background: white;
        border-bottom: 5px solid rgb(142, 253, 142);
        height: 7vh;
        width: 100%;
    }
    .cabecera a{
        text-decoration: none;
        padding-inline: 20px;
        color: black;
        font-size: 20px;
    }
</style>

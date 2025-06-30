<script setup>
import Proyecto from './Proyecto.vue';

import portadaRapidWeather from '../assets/rapidweather.png'
import portadaBenchFitness from '../assets/benchfitness.png'

import flutterLogo from '../assets/flutter.png'
import kotlinLogo from '../assets/kotlin.png'
import jetpackcomposeLogo from '../assets/jetpackcompose.png'
import firebaseLogo from '../assets/firebase.png'


const rapidWeather = {
    imgUrl: portadaRapidWeather,
    titulo: 'RapidWeather',
    colorTitulo: "#4A90E2",
    enlaces: [
        {
            id: 1, svg: `<svg xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 30 30">
                            <path fill="currentColor"
                                d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z" />
                        </svg>`, tamanyo: "35px", enlace: "https://github.com/OscarLuque-31/Rapid-Weather"
        },
        {
            id: 2, svg: `<svg version="1.1" id="Icons" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
                      viewBox="0 0 32 32" xml:space="preserve">
                  <g>
                      <path fill="currentColor" d="M17,14.5l4.2-4.5L4.9,1.2C4.8,1.1,4.6,1.1,4.3,1L17,14.5z"/>
                      <path fill="currentColor" d="M23,21l5.9-3.2c0.7-0.4,1.1-1,1.1-1.8s-0.4-1.5-1.1-1.8L23,11l-4.7,5L23,21z"/>
                      <path fill="currentColor" d="M2.4,1.9C2.1,2.2,2,2.6,2,3V29c0,0.4,0.1,0.8,0.4,1.2L15.6,16L2.4,1.9z"/>
                      <path fill="currentColor" d="M17,17.5L4.3,31c0.2,0,0.4-0.1,0.6-0.2L21.2,22L17,17.5z"/>
                  </g>"
                  </svg>`, tamanyo: "30px", enlace: "https://play.google.com/store/apps/details?id=com.app.rapid_weather"
        }
    ],
    subtitulo: 'RapidWeather es una aplicación móvil moderna y eficiente, desarrollada con Flutter y Dart, que te permite acceder a la información meteorológica más reciente de tu ubicación al instante.',
    tecnologias: [
        { id: 1, imgUrl: flutterLogo, nombre: 'Flutter', backgroundColor: '#3FC3FE' },
        { id: 2, imgUrl: firebaseLogo, nombre: 'Firebase', backgroundColor: '#FE9000' }
    ]
};

const benchfitness = {
    imgUrl: portadaBenchFitness,
    titulo: 'Bench Fitness',
    colorTitulo: "#E63946",
    enlaces: [
        {
            id: 1, svg: `<svg xmlns="http://www.w3.org/2000/svg"
                            viewBox="0 0 30 30">
                            <path fill="currentColor"
                                d="M15,3C8.373,3,3,8.373,3,15c0,5.623,3.872,10.328,9.092,11.63C12.036,26.468,12,26.28,12,26.047v-2.051 c-0.487,0-1.303,0-1.508,0c-0.821,0-1.551-0.353-1.905-1.009c-0.393-0.729-0.461-1.844-1.435-2.526 c-0.289-0.227-0.069-0.486,0.264-0.451c0.615,0.174,1.125,0.596,1.605,1.222c0.478,0.627,0.703,0.769,1.596,0.769 c0.433,0,1.081-0.025,1.691-0.121c0.328-0.833,0.895-1.6,1.588-1.962c-3.996-0.411-5.903-2.399-5.903-5.098 c0-1.162,0.495-2.286,1.336-3.233C9.053,10.647,8.706,8.73,9.435,8c1.798,0,2.885,1.166,3.146,1.481C13.477,9.174,14.461,9,15.495,9 c1.036,0,2.024,0.174,2.922,0.483C18.675,9.17,19.763,8,21.565,8c0.732,0.731,0.381,2.656,0.102,3.594 c0.836,0.945,1.328,2.066,1.328,3.226c0,2.697-1.904,4.684-5.894,5.097C18.199,20.49,19,22.1,19,23.313v2.734 c0,0.104-0.023,0.179-0.035,0.268C23.641,24.676,27,20.236,27,15C27,8.373,21.627,3,15,3z" />
                        </svg>`, tamanyo: "35px", enlace: "https://github.com/OscarLuque-31/BenchFitness"
        }
    ],
    subtitulo: 'BenchFitness es una aplicación móvil para Android enfocada en usuarios de gimnasio que desean llevar un control completo y personalizado de su progreso.',
    tecnologias: [
        { id: 1, imgUrl: kotlinLogo, nombre: 'Kotlin', backgroundColor: '#7B70E3' },
        { id: 2, imgUrl: jetpackcomposeLogo, nombre: 'Jetpack Compose', backgroundColor: '#36BE6D' },
        { id: 3, imgUrl: firebaseLogo, nombre: 'Firebase', backgroundColor: '#FE9000' }
    ]
};

const pixelhub = {
    imgUrl: portadaRapidWeather,
    titulo: 'RapidWeather',
    subtitulo: 'Una aplicación del tiempo moderna y responsiva.',
    tecnologias: [
        { id: 1, imgUrl: flutterLogo, nombre: 'Flutter', backgroundColor: '#3FC3FE' }
    ]
};

</script>

<template>
    <div class="contenedorProyectos" id="proyectos">
        <h1>Proyectos</h1>
        <div class="proyectos">
            <Proyecto 
            :imgUrl="rapidWeather.imgUrl" 
            :titulo="rapidWeather.titulo"
            :colorTitulo="rapidWeather.colorTitulo" 
            :subtitulo="rapidWeather.subtitulo"
            :tecnologias="rapidWeather.tecnologias" 
            :enlaces="rapidWeather.enlaces" />

            <Proyecto :imgUrl="benchfitness.imgUrl" 
            :titulo="benchfitness.titulo"
            :colorTitulo="benchfitness.colorTitulo" 
            :subtitulo="benchfitness.subtitulo"
            :tecnologias="benchfitness.tecnologias" 
            :enlaces="benchfitness.enlaces" />
        </div>
    </div>
</template>

<style scoped>
.proyectos {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    justify-content: space-around;
    gap: 50px;
}

.contenedorProyectos {
    min-height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: white;
}
</style>

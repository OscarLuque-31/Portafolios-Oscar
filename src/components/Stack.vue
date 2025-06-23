<script setup>
import flutterLogo from '../assets/flutter.png'
import javaLogo from '../assets/java.png'
import kotlinLogo from '../assets/kotlin.png'
import htmlLogo from '../assets/html.webp'
import mysqlLogo from '../assets/mysql.svg'
import cssLogo from '../assets/css.svg'
import springLogo from '../assets/spring.png'
import gitLogo from '../assets/git.png'
import firebaseLogo from '../assets/firebase.png'
import jetpackcomposeLogo from '../assets/jetpackcompose.png'
import TarjetaTecnologia from './TarjetaTecnologia.vue';



</script>

<template>
    <div class="stack">
        <h1>Stack</h1>
        <div class="tarjetas">
            <TarjetaTecnologia :imgUrl=javaLogo backgroundColor="#DA370D" />
            <TarjetaTecnologia :imgUrl=kotlinLogo backgroundColor="#7B70E3" />
            <TarjetaTecnologia :imgUrl=mysqlLogo backgroundColor="#006089" />
            <TarjetaTecnologia :imgUrl=springLogo backgroundColor="#6EAB4F" />
            <TarjetaTecnologia :imgUrl=gitLogo backgroundColor="#F3501D" />
            <TarjetaTecnologia :imgUrl=htmlLogo backgroundColor="#E83E2E" />
            <TarjetaTecnologia :imgUrl=cssLogo backgroundColor="#1B87C6" />
            <TarjetaTecnologia :imgUrl=jetpackcomposeLogo backgroundColor="#36BE6D" />
        </div>
        <div class="tarjetas">
            <TarjetaTecnologia :imgUrl=flutterLogo backgroundColor="#3FC3FE" />
            <TarjetaTecnologia :imgUrl=firebaseLogo backgroundColor="#FE9000" />

        </div>
    </div>
</template>

<style>
.stack {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 40vh;
    color: white;
}

.tarjetas {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    color: white;
    height: 11vh;
}
</style>

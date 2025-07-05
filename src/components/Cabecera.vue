<script setup>
import { ref } from 'vue';

// Estado para controlar si el menú móvil está abierto o cerrado
const menuAbierto = ref(false);

// Función para alternar el estado del menú
const alternarMenu = () => {
  menuAbierto.value = !menuAbierto.value;
};
</script>

<template>
  <header class="cabecera">
    <button class="boton-menu-hamburguesa" @click="alternarMenu">
      <span class="linea"></span>
      <span class="linea"></span>
      <span class="linea"></span>
    </button>

    <nav :class="{ 'menu-activo': menuAbierto }">
      <a href="#presentacion" @click="menuAbierto = false">Inicio</a>
      <a href="#sobremi" @click="menuAbierto = false">Sobre mí</a>
      <a href="#experiencia" @click="menuAbierto = false">Experiencia</a>
      <a href="#proyectos" @click="menuAbierto = false">Proyectos</a>
    </nav>
  </header>
</template>

<style scoped>
/* ===============================
   BASE: TODO ES PARA MÓVIL
   =============================== */
.cabecera {
  display: flex;
  justify-content: flex-end; /* Alineado a la derecha para el botón */
  align-items: center;
  background: white;
  border-bottom: 5px solid rgb(142, 253, 142);
  height: 7vh;
  width: 100%;
  z-index: 1000;
  box-sizing: border-box;
  padding-right: 20px; /* Padding para el botón */
}

/* El botón hamburguesa está visible POR DEFECTO */
.boton-menu-hamburguesa {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  width: 30px; 
  height: 25px; 
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 1001; /* Debe estar por encima del nav */
}

.boton-menu-hamburguesa .linea {
  width: 100%;
  height: 3px; 
  background-color: black;
  border-radius: 2px;
}

/* El menú NAV está oculto y con estilo móvil POR DEFECTO */
.cabecera nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(255, 255, 255, 0.97); 
  display: flex; /* Sigue siendo flex para centrar contenido */
  flex-direction: column; 
  justify-content: center; 
  align-items: center;
  transform: translateX(100%); /* Oculto fuera de la pantalla */
  transition: transform 0.4s ease-in-out;
  z-index: 999; 
}

/* Se muestra cuando la clase .menu-activo está presente */
.cabecera nav.menu-activo {
  transform: translateX(0); 
}

/* Los enlaces tienen estilo móvil POR DEFECTO */
.cabecera nav a {
  font-size: 28px; 
  padding: 15px 0;
  width: 80%; 
  text-align: center;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
  text-decoration: none;
  color: black;
}
.cabecera nav a:last-child {
  border-bottom: none; 
}


/* ===============================
   AJUSTES PARA PANTALLAS GRANDES
   (a partir de 601px)
   =============================== */
@media (min-width: 601px) {
  /* Ocultamos el botón hamburguesa */
  .boton-menu-hamburguesa {
    display: none;
  }

  /* Devolvemos el NAV a su estado de escritorio */
  .cabecera nav {
    position: static; /* Clave: ya no está fijo */
    transform: translateX(0); /* Clave: lo devolvemos a su sitio */
    flex-direction: row; /* Clave: horizontal de nuevo */
    background: none; /* Quitamos el fondo */
    height: auto;
    width: auto;
  }
  
  /* Devolvemos los enlaces a su estado de escritorio */
  .cabecera nav a {
    font-size: 20px;
    padding: 10px 20px;
    width: auto;
    border-bottom: none; /* Quitamos el borde móvil */
  }

  /* Restauramos el hover de escritorio */
  .cabecera a:hover {
    background-color: rgba(142, 253, 142, 0.5); 	
  }

  /* Restauramos la alineación del header */
  .cabecera {
    justify-content: space-around;
    padding-right: 0;
  }
}
</style>
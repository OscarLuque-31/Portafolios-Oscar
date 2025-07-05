<script setup>
</script>

<template>
    <div id="experiencia">
        <h1>Experiencia</h1>
        <section class="seccionExp">
            <div class="nombreFecha">
                <h1>Becario</h1>
                <h2>Accenture</h2>
                <h3>11/2024 - 06/2025</h3>
            </div>
            <div class="detallesExp">
                <ul>
                    <li>Desarrollo en frontend utilizando Vue y React.</li>
                    <li>Desarrollo en backend con Java y entorno APX.</li>
                    <li>Prácticas con alguna librería de APX Online y Batch.</li>
                    <li>Obtuve certificaciones internas de BBVA en APX, ASO y LRBA.</li>
                </ul>
            </div>
        </section>
        <br>
        <section class="seccionExp">
            <div class="nombreFecha">
                <h1>Estudiante en prácticas duales</h1>
                <h2>Accenture</h2>
                <h3>03/2024 - 05/2024</h3>
            </div>
            <div class="detallesExp">
                <ul>
                    <li>
                        Colaboración en equipo.
                    </li>
                    <li>
                        Introducción práctica a tecnologías como JSP y Servlets.
                    </li>
                    <li>
                        Mejora de habilidades en control de versiones con GitHub.
                    </li>

                </ul>
            </div>
        </section>
    </div>
</template>

<style scoped>
#experiencia {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: auto;
  color: white;
  padding-inline: 20px; 
}

.seccionExp {
  width: 100%; 
  color: white;
  margin-bottom: 20px;
}

.nombreFecha {
  display: flex;
  flex-direction: column;
  gap: 10px; 
  border-left: 3px solid rgb(142, 253, 142);
  margin-block: 10px;
}

.nombreFecha h1,
.nombreFecha h2,
.nombreFecha h3 {
  margin: 0;
  padding: 0;
  padding-left: 20px;
}

.nombreFecha h1{
  color: rgb(142, 253, 142);
}

.nombreFecha h2 {
  font-size: 22px;
  font-weight: 500;
}

.nombreFecha h3 {
  font-size: 15px;
  margin-bottom: 10px;
  opacity: 0.9;
  font-weight: 500;
}

.detallesExp {
  background: rgba(142, 253, 142, 0.15);
  border: 1px solid rgba(142, 253, 142, 0.4);
  border-radius: 10px;
  padding: 15px; 
  font-family: "League Spartan", sans-serif;
  font-size: 20px; 
  color: white;
  transition: all 0.3s ease;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.detallesExp ul {
  padding-left: 20px; 
}

.detallesExp ul li {
  margin-bottom: 20px;
}


@media (min-width: 768px) {
  #experiencia {
    padding-inline: 0;
  }

  .seccionExp {
    width: 80%;
  }

  .detallesExp {
    font-size: 20px; 
  }
}


@media (min-width: 1024px) {
  .seccionExp {
    width: 45vw;
  }

  .nombreFecha h2 {
    font-size: 22px;
  }

  .nombreFecha h3 {
    font-size: 15px;
  }

  .detallesExp {
    font-size: 20px; 
  }
}
</style>

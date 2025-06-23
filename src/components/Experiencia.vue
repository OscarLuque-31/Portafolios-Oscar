<script setup>
</script>

<template>
    <div id="experiencia">
        <h1>Experiencia</h1>
        <section class="seccionExp">
            <div class="nombreFecha">
                <h2>Accenture - Becario</h2>
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
                <h2>Accenture - Dual</h2>
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
    height: 80vh;
    color: white;

}

.seccionExp {
    width: 40vw;
    color: white;
}

.nombreFecha {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}

.nombreFecha h2 {
    color: rgb(142, 253, 142);
}

.detallesExp {
    background-color: blue;
    border-radius: 10px;
    padding: 10px;
    font-family: "League Spartan", sans-serif;
    font-size: 18px;
    background: rgba(142, 253, 142, 0.15);
    /* Vidrioso */
    backdrop-filter: blur(10px);
    /* Difuminado */
    -webkit-backdrop-filter: blur(10px);
    /* Safari */
    border: 1px solid rgba(142, 253, 142, 0.4);
    /* Borde suave */
    color: white;
    transition: all 0.3s ease;
    padding: 10px;
    gap: 8px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
}

.detallesExp ul li {
    margin-bottom: 20px;
    /* Puedes ajustar el valor a tu gusto */
}
</style>

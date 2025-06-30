<script setup>
</script>

<template>
    <footer class="footer">
        <div class="contenidofooter">
            <p class="informacion-contacto">
                Contacto: <span class="email">oscarluquehidalgo@gmail.com</span>
            </p>
            <p class="derechos-de-autor">
                &copy; 2025 Óscar Luque Hidalgo
            </p>
        </div>
    </footer>
</template>

<style scoped>
.footer {
    background: #1a1a1a;
    color: #f4f4f4;
    padding: 20px 20px;
    text-align: center;
    border-top: 1px solid rgba(142, 253, 142, 0.2);

}

.contenidofooter {
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
}

.derechos-de-autor {
    font-size: 0.9em;
    opacity: 0.8;
}

.informacion-contacto a {
    color: #8efd8e;
    text-decoration: none;
    transition: color 0.3s ease;
}

.email {
    color: #8efd8e;
    text-decoration: none;
    transition: color 0.3s ease;
}

.informacion-contacto a:hover {
    text-decoration: underline;
    color: #a4ffb0;
}

@media (max-width: 600px) {
    .footer {
        padding: 30px 15px;
    }
}
</style>
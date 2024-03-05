<script setup>
    import { ref } from 'vue'
    import paso_1 from '../assets/img/paso_1.png'
    import paso_2 from '../assets/img/paso_2.png'
    import paso_3 from '../assets/img/paso_3.png'

    const pasos = ref([
        {rutaImagen: paso_1},
        {rutaImagen: paso_2},
        {rutaImagen: paso_3}
    ])


</script>

<template>
    <section class="pasos">
        <img class="pasos__wave" src="../assets/img/wave.svg" alt="imagen wave">

        <div class="pasos__contenido">
            <h2 class="pasos__heading">¿Cómo funciona? <span class="pasos__heading--descripcion">tan fácil como 1,2 y
                    3</span></h2>
            <div class="pasos__grid contenedor">
                <div v-for="(paso, index) in pasos" :key="index"  class="pasos__paso">
                    <img class="pasos__imagen" :src="paso.rutaImagen" alt="imagen paso app">
                </div>
            </div>
        </div>
    </section>

</template>

<style scoped></style>
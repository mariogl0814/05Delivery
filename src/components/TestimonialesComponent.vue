<script setup>
    import { ref } from 'vue';
    import testimonial1 from '../assets/img/testimonial1.jpg'
    import testimonial2 from '../assets/img/testimonial2.jpg'
    import testimonial3 from '../assets/img/testimonial3.jpg'
    import testimonial4 from '../assets/img/testimonial4.jpg'
    import testimonial5 from '../assets/img/testimonial5.jpg'
    import estrellas from '../assets/img/estrellas.png'

    const rutaEstrella = estrellas
    const testimoniales = ref([
        {
            autor: 'Juan Perez',
            rutaImagen: testimonial1,
            texto: 'Una excelente app, puedo seleccionar de una gran cantidad de opciones y pagar en tarjeta o efectivo según me convenga.'
        },
        {
            autor: 'Ana Rodriguez',
            rutaImagen: testimonial2,
            texto: 'Increíble aplicación, me encanta la variedad de opciones disponibles y la facilidad para realizar pagos, ya sea con tarjeta o en efectivo.'
        },
        {
            autor: 'Luis Gomez',
            rutaImagen: testimonial3,
            texto: 'Una app fantástica, la diversidad de elecciones es asombrosa y la posibilidad de pagar con tarjeta o en efectivo hace que sea muy conveniente.'
        },
        {
            autor: 'Maria Fernandez',
            rutaImagen: testimonial4,
            texto: 'Esta aplicación es genial, puedo elegir entre tantas opciones y la flexibilidad de pago con tarjeta o en efectivo es muy útil.'
        },
        {
            autor: 'Carla Martinez',
            rutaImagen: testimonial5,
            texto: 'Una app destacada, la amplia gama de opciones disponibles es impresionante y la facilidad para realizar pagos con tarjeta o en efectivo es muy conveniente.'
        }
    ])


</script>

<template>
    <section class="contenedor testimoniales">
        <h2 class="testimoniales__heading">Testimoniales</h2>

        <div class="testimoniales__grid">
            <div v-for="(testimonial, index) in testimoniales" :key="index" class="testimonial">
                <header class="testimonial__header">
                    <div class="testimonial__imagen">
                        <img :src="testimonial.rutaImagen" alt="testimonial">
                    </div>

                    <div class="testimonial__informacion">
                        <p class="testimonial__autor">{{ testimonial.autor }}</p>
                        <img class="testimonial__calificacion" :src="estrellas" alt="imagen estrellas">
                    </div>
                </header>

                <blockquote class="testimonial__texto">{{ testimonial.texto }}</blockquote>
            </div> <!--.testimonial-->

        </div>
    </section>

</template>

<style scoped></style>
<script lang="ts" setup>
    import {ref} from 'vue'
    import ensaladas from '../assets/img/logo_ensaladas.png'
    import estrellas from '../assets/img/estrellas.png'

    const favorito = ref({
        nombre: 'Green Ensaladas',
        descripcion: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nemo eos ullam mollitia et sit sequi est perspiciatis qui, ex, iure sed! Ducimus magnam eveniet fugit atque maxime architecto necessitatibus esse.'
    })

</script>

<template>
    <main class="favoritos">
        <h2 class="favoritos__heading">Restaurantes Favoritos</h2>

        <div class="favoritos__grid contenedor">
            <div v-for="n in 6" :key="n" class="favorito">
                <div class="favorito__grid">
                    <div class="favorito__imagen">
                        <img :src="ensaladas" alt="logo restaurant">
                    </div>

                    <div class="favorito__contenido">
                        <img :src="estrellas" alt="calificacion restaurant">

                        <h3 class="favorito__nombre">{{ favorito.nombre }}</h3>
                        <p class="favorito__descripcion">{{ favorito.descripcion }}</p>
                    </div>
                </div>
            </div> <!--.favorito-->

        </div>
    </main>

</template>

<style scoped></style>
<script lang="ts" setup>

</script>

<template>
    <section class="contenedor formulario">
        <div class="formulario__grid">
            <div class="formulario__contenido">
                <h2 class="formulario__heading">Encuentra y Pide comida de tu restaurante favorito</h2>
                <form class="formulario__buscar">
                    <div class="formulario__campo">
                        <label for="restaurant" class="formulario__label">Restaurant</label>
                        <input id="restaurant" class="formulario__input" placeholder="Tacos México">
                    </div>
                    <div class="formulario__campo">
                        <label for="platillo" class="formulario__label">Platillo</label>
                        <input id="platillo" class="formulario__input" placeholder="Pizza, Ensalada, Hamburguesa">
                    </div>
                    <input type="submit" class="formulario__submit" value="Buscar">
                </form>
            </div>
            <div class="formulario__imagen-contenedor">
                <img class="formulario__imagen" src="../assets/img/dibujo_repartidor.svg" alt="imagen repartidor">
            </div>
        </div>
    </section>
</template>

<style scoped></style>
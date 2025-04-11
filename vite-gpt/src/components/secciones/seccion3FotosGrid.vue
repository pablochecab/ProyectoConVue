<script setup>
import { ref } from 'vue'
import Tarjeta from '../tarjetas/tarjetaFotoDescripcion.vue'

// Declaración correcta de las imágenes
const imagenes = ref([
    {
        title: "Mercurio",
        url: "mercurio.jpg"
    },
    {
        title: "Tierra",
        url: "tierra.jpg"
    },
    {
        title: "Saturno",
        url: "saturno.jpg"
    }
]);
console.log("imagenes",imagenes.value)
</script>

<template>
  <section>
    <!-- Pasamos las imágenes como propiedades al componente Tarjeta -->
    <template v-for="img in imagenes">
        <Tarjeta :title="img.title" :img="img.url"/>
    </template>
  </section>
</template>

<style>
  section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    column-gap: 2em;
    padding: 2em;
  }
</style>

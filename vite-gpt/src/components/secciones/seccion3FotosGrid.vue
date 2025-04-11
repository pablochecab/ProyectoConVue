<script setup>
import { ref } from 'vue'
import Tarjeta from '../tarjetas/tarjetaFotoDescripcion.vue'

// Declaración correcta de las imágenes
const imagenes = ref([
    {
        title: "Titulo1",
        url: "fondo.jpg"
    },
    {
        title: "Titulo2",
        url: "fondo.jpg"
    },
    {
        title: "Titulo3",
        url: "fondo.jpg"
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
    background-image: url();
  }
</style>

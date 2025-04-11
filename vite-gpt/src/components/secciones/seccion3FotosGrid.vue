<script setup>
import { ref } from 'vue'
import Tarjeta from '../tarjetas/tarjetaFotoDescripcion.vue'

// Creamos una constante "array" que dentro guarda objetos con los atributos url y titulo, facilitando su paso a otra clase.
const objetos = ref([
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

//Comprobamos que funciona
console.log("objetos",objetos.value)
</script>

<template>
  <section>
    <!-- Pasamos por cada objeto en la array, con props a tarjetaFotoDescripcion -->
    <template v-for="objeto in objetos">
        <Tarjeta :title="objeto.title" :img="objeto.url"/>
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

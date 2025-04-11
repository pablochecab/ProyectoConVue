<script setup>
import Section1 from './secciones/seccion3fotosGrid.vue'
import Button from './botones/boton.vue'
import { provide, ref } from 'vue'

// Hacer la variable reactiva
const mostrarSeccionExtra = ref(false)

function cargarNuevaSeccion() {
  mostrarSeccionExtra.value = !mostrarSeccionExtra.value
}

provide('cargarSeccion', cargarNuevaSeccion)
</script>

<template>
  <main>
    <section class="s">
      <h1><slot name="titulo">Main de la pagina</slot></h1>
      <p><slot name="descripcion">Fotos de la galaxia:</slot></p>
    </section>

    <Section1 />
    <Button />
    <Section1 v-if="mostrarSeccionExtra" />
  </main>
</template>

<style scoped>
main {
  background: #f80404;
  color: white;
}

.s {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>

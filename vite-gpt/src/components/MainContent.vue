<script setup>
import Section1 from './secciones/seccion3fotosGrid.vue'
import Button from './botones/boton.vue'
import { provide, ref } from 'vue'

// Hacer la variable reactiva
const mostrarSeccionExtra = ref(false)

function cargarNuevaSeccion() {
  mostrarSeccionExtra.value = !mostrarSeccionExtra.value
}
// Proveemos la funcion al archivo "boton.vue"
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
    <!-- Añadimos una condición de que solo se muestre si es verdadero. -->
    <Section1 v-if="mostrarSeccionExtra" />
    <!-- Como idea para practicar podriamos hacer que cada vez que se haga click a otro botón, se cree una sección nueva. -->
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

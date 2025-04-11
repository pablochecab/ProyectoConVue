<script setup>
import Section1 from './secciones/seccion3fotosGrid.vue'
</script>

<template>
  <main>
    <h1><slot name="titulo">Main de la pagina</slot></h1>
    <p><slot name="descripcion">Descripcion del main</slot></p>
    <Section1 />
  </main>
</template>

<style scoped>
main {
  background: #f80404;
  color: white;
}
</style>
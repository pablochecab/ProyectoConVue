<script setup>
import { inject } from 'vue'

// Recibimos el archivo de MainContent, para así aquí poder programar que el botón ejecute esa función.
const toggleNewSection = inject('cargarSeccion')
</script>

<template>
  <div>
    <!-- Utilizamos un EventListener para que cuando se hace click, ejecute la funcion. -->
    <button @click="toggleNewSection">Ver más</button>
  </div>
</template>

<style scoped>
div {
  display: flex;
  justify-content: center;
}

button {
  padding: 1em 2em;
  background-color: darkblue;
  color: white;
  border: solid 1px white;
  margin-bottom: 2em;
}
button:hover {
  background-color: rgb(0, 0, 0);
  transition: 1s;
  box-shadow: 0px 10px 30px rgb(0, 0, 0);
  transform: translateY(-5px);
  cursor: pointer;
}
</style>

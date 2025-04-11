<script setup>
import { ref } from 'vue'
import Header from './components/Header.vue'
import MainContent from './components/MainContent.vue'
import Footer from './components/Footer.vue'

const nombreEmpresa = ref('Blanco Media Web')
const descripcionEmpresa = ref('Expertos en fotografía y diseño web')
</script>

<template>
  <body>
    <!-- Ejemplo de como pasar props, en este caso al header -->
    <Header :titulo="nombreEmpresa" :descripcion="descripcionEmpresa" />
    <!-- Ejemplo de como sustituir un slot -->
    <MainContent #titulo>
      La galaxia a otro nivel
    </MainContent>
    
    <Footer />
  </body>
</template>

<style>
  body {
    background-color: green;
  }
</style>
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
    <Header :titulo="nombreEmpresa" :descripcion="descripcionEmpresa" />
    
    <MainContent #titulo>
      TITULO DEL MAIN
    </MainContent>
    
    <Footer />
  </body>
</template>

<style>
  body {
    background-color: green;
  }
</style>
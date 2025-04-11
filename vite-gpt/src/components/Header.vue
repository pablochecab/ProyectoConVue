<script setup>
import Nav from './navs/navTransparente.vue'

const props = defineProps({
  titulo: String,
  descripcion: String,
  navItems: Array // Solo definir la estructura aquí
})

// Si quieres pasar valores a 'navItems', deberías hacerlo al usar el componente <Nav />
</script>

<template>
  <header>
    <section class="s1">
      <h1>{{ titulo || 'BIENVENIDO' }}</h1>
      <p>{{ descripcion || 'Breve descripción' }}</p>
    </section>
    <section class="s2">
      <!-- Pasar navItems directamente -->
      <Nav :navItems="[
        { name: 'Inicio', link: '/' },
        { name: 'Servicios', link: '/servicios' },
        { name: 'Acerca de', link: '/acerca' },
        { name: 'Portafolio', link: '/portafolio' },
        { name: 'Blog', link: '/blog' },
        { name: 'Contacto', link: '/contacto' }
      ]" />
    </section>
  </header>
</template>

<style scoped>
header {
  background-image: url('../../public/fondo.jpg');
  color: white;
  padding: 1rem;
  height: 100vh;
  display: flex;
  justify-content: space-between;
}

h1 {
  font-size: 50pt;
}

.s1 {
  align-self: end;
}

.s2 {
  align-self: self-start;
}
</style>


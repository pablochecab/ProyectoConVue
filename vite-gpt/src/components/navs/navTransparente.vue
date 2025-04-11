<script setup>
defineProps({
  navItems: Array // Definir 'navItems' como una propiedad
})
</script>

<template>
    <nav>
      <!-- Iterar sobre los navItems y asignar clases dinámicas como nav0, nav1, nav2, etc... -->
      <p v-for="(item, index) in navItems" :key="index" :class="'nav' + index">
        <a :href="item.link">{{ item.name }}</a>
      </p>
    </nav>
  </template>

<style scoped>
nav {
  display: flex;
  background-color: rgba(0, 17, 255, 0);
}

nav p {
  border-right: solid 1px white;
  padding: 0em 1em;
  font-size: 15pt;
  text-transform: uppercase;
}

nav p a:hover {
    cursor: pointer;
    color: gold;
}

nav p a {
  color: white;
  text-decoration: none;
}

.nav5 {
  border-right: none;
}
</style>

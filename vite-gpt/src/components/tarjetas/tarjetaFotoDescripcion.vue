<script setup>

// Definimos los props que sabemos que nos van a llegar.
const props = defineProps({
  title: String,
  img: String
});

// Seteamos la URL como string en una variable, importante usar esas comillas, que son las que permiten meter atributos.
const url = `/${props.img}`;
</script>

<template>
  <article>
    <!-- Metemos la const definida arriba con su valor, que será el del prop que nos ha llegado. -->
    <img :src="url" alt="Imagen" />
    <!-- Utilizamos el mustache para cambiar el texto por lo que nos llegue en el prop. -->
    <p>{{ props.title }}</p>
  </article>
</template>

<style scoped>
article {
  background-color: #eee;
  text-align: center;
  border: solid 2px black;

}

p {
  color: black;
}

img {
  width: 100%;
  height: auto;
}

</style>


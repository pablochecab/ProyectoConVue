<script setup>
const props = defineProps({
  title: String,
  img: String
});

// Como la imagen está directamente en /public, no necesitas carpeta assets
const url = `/${props.img}`;
</script>

<template>
  <article>
    <img :src="url" alt="Imagen" />
    <p>{{ props.title }}</p>
  </article>
</template>

<style scoped>
article {
  padding: 1rem;
  background-color: #eee;
  text-align: center;
}

img {
  width: 50%;
  height: auto;
}
</style>


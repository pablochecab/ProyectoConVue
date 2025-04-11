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


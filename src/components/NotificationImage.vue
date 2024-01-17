<template>
  <div class="imageList">
    <template v-for="(image, index) in imagesList" v-bind:key="image">
      <img :src="image" :alt="`perfil${index}`" />
    </template>
  </div>
</template>

<script>
export default {
  props: {
    imagesList: Array,
  },
}
</script>

<style scoped>
.imageList {
  position: relative;

  width: 3.5em;
  height: 2em;
  margin-left: 0.5em;
}
img {
  position: absolute;

  height: calc(2em - 0.35em);
  aspect-ratio: 1;
  border-radius: 50%;
  border: 0.2em solid white;
}
img:nth-child(1) {
  left: 0;
}
img:nth-child(2) {
  left: 1em;
}
img:nth-child(3) {
  left: 2em;
}
</style>

<template>
  <div class="imageList">
    <img src="../assets/images/perfilDisney1.jpg" alt="perfil1" />
    <img src="../assets/images/perfilDisney2.jpg" alt="perfil2" />
    <img src="../assets/images/perfilDisney3.jpg" alt="perfil3" />
  </div>
</template>

<style scoped>
.imageList {
  position: relative;
  height: 2em;
}
img {
  position: absolute;

  width: 1.5em;
  aspect-ratio: 1;
  border-radius: 50%;
  border: 3px solid white;
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

<template>
  <li class="containerItem">
    <img :src="src" alt="frontImage" class="imgList" />
    <div class="infoContainer">
      <span class="title"> {{ title }} </span>
      <span class="infos"
        >{{ author }} * {{ category }} * {{ year }} * {{ pages }}
        {{ $t("Pages") }}</span
      >
    </div>
  </li>
</template>

<script>
export default {
  name: "ListItemComponent",
  props: {
    src: String,
    title: String,
    author: String,
    category: String,
    year: Number,
    pages: Number,
  },
}
</script>
<style>
.containerItem {
  background-color: transparent;
  color: var(--color-title-item);

  display: flex;
  align-items: center;
  justify-content: flex-start;

  border-radius: 0.5em;

  margin: 0.5em;
  padding: 0.5em;
  height: 4em;

  cursor: pointer;
  user-select: none;
}
.containerItem:hover {
  background-color: var(--background-item-hover);
}
.imgList {
  background-color: var(--background-image-item);

  height: calc(100% - 1em);
  aspect-ratio: 3 / 4;

  padding-block: 0.5em;
  padding-inline: 0.8em;

  border-radius: 0.5em;
}
.infoContainer {
  display: flex;
  flex-direction: column;

  justify-content: space-evenly;

  margin-left: 1em;

  height: 100%;
}
.title {
  font-weight: bold;
}
.infos {
  color: var(--color-item-description);
  font-size: small;
}
</style>

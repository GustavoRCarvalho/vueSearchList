<template>
  <div class="notificationBlur">
    <button class="notificationButton">
      3 {{ $t("BooksAdded") }}
      <NotificationImage :imagesList="imagesList" />
    </button>
  </div>
</template>

<script setup>
import NotificationImage from "./NotificationImage.vue"
import perfil1 from "../assets/images/perfilDisney1.jpg"
import perfil2 from "../assets/images/perfilDisney2.jpg"
import perfil3 from "../assets/images/perfilDisney3.jpg"

const imagesList = [perfil1, perfil2, perfil3]
</script>

<style>
.notificationBlur {
  position: absolute;
  bottom: 0;
  left: 0;

  display: flex;
  align-items: flex-end;
  justify-content: center;

  backdrop-filter: blur(5px);

  padding-bottom: 1em;
  height: 6em;
  width: 100%;
}
.notificationButton {
  display: flex;
  align-items: center;
  background-color: var(--background-white-light);

  font-family: Inter, Helvetica, Arial, sans-serif;
  font-weight: bold;

  padding-block: 0.4em;
  padding-inline: 1.4em;

  border: none;
  border-radius: 5em;

  cursor: pointer;
}
</style>

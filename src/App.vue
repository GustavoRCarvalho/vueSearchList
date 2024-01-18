<template>
  <SearchPage />
  <button v-on:click="setLocale">{{ locale }}change language to pt</button>
</template>

<script setup>
import { ref } from "vue"
import SearchPage from "./components/SearchPage.vue"
import { useI18n } from "vue-i18n"

const t = useI18n()

const locale = ref("en")

function setLocale() {
  console.log("asdasd")
  t.locale.value = "pt"
}
document.title = "Vue Search App"
</script>

<style>
@font-face {
  font-family: Inter;
  src: url("~@/assets/fonts/Inter-Regular.ttf");
}
#app {
  font-family: Inter, Helvetica, Arial, sans-serif;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  width: 100%;
  height: 100%;
}
body {
  --background-gray-dark: #131313;
  --background-gray-medium: #1a1a1a;
  --background-gray-medium-light: #252525;
  --background-gray-light: #363636;
  --background-red-dark: #301f18;
  --background-white-light: #fff;
  --color-white-medium: #e4e4e4;
  --color-red-medium: #dd5107;
  --color-gray-medium: #3f3f43;
  --color-gray-light: #797979;
  display: flex;
  align-items: center;
  justify-content: center;

  min-height: 100dvh;
  min-width: 100dvw;
  margin: 0;

  background-color: var(--background-gray-dark);
}
</style>

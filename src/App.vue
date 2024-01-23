<template>
  <header>
    <ChangeColorTheme />
    <ChangeLanguage />
  </header>
  <main>
    <SearchPage />
  </main>
</template>

<script setup>
import ChangeColorTheme from "./components/ChangeColorTheme.vue"
import ChangeLanguage from "./components/ChangeLanguage.vue"
import SearchPage from "./components/SearchPage.vue"

document.title = "Vue Search App"

const bodyElement = document.body
bodyElement.classList.add("light-theme")
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
}
.light-theme {
  --background-white-light: #fff;
  --background-app: #ececec;
  --background-card: #e6e6e6;
  --background-item-hover: #dadada;
  --background-image-item: #cacaca;
  --background-button-search: #f1b094;
  --background-button-theme: #363636;
  --color-button-theme: #ececec;
  --color-title-item: #1b1b1b;
  --color-button-search: #572003;
  --color-item-description: #c0c0bc;
  --color-list-title: #3a3a3a;
}
.dark-theme {
  --background-white-light: #fff;
  --background-app: #131313;
  --background-card: #1a1a1a;
  --background-item-hover: #252525;
  --background-image-item: #363636;
  --background-button-search: #301f18;
  --background-button-theme: #ececec;
  --color-button-theme: #131313;
  --color-title-item: #e4e4e4;
  --color-button-search: #dd5107;
  --color-item-description: #3f3f43;
  --color-list-title: #797979;
}
body {
  display: flex;
  align-items: center;
  justify-content: center;

  margin: 0;

  background-color: var(--background-app);
}
header {
  position: sticky;
  top: 0;

  width: 100%;

  padding-block: 1em;

  display: flex;
  justify-content: center;
  align-items: center;
}
main {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  min-height: 70dvh;
  width: 100%;
}
</style>

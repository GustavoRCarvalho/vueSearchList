<template>
  <header>
    <ChangeLanguage />
  </header>
  <main>
    <SearchPage />
  </main>
</template>

<script setup>
import ChangeLanguage from "./components/ChangeLanguage.vue"
import SearchPage from "./components/SearchPage.vue"

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

  margin: 0;

  background-color: var(--background-gray-dark);
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

<template>
  <button type="button" v-on:click="changeTheme">
    <MoonIcon class="icon" />{{ themeLabel(themeDark) }}
    <SunIcon class="icon" />
  </button>
</template>

<script setup>
import { MoonIcon } from "@heroicons/vue/24/outline"
import { SunIcon } from "@heroicons/vue/24/solid"
import { ref } from "vue"

const bodyElement = document.body
const themeDark = ref(bodyElement.classList.contains("dark-theme"))

function themeLabel(theme) {
  return theme ? "Dark" : "Light"
}

function changeTheme() {
  if (themeDark.value === true) {
    themeDark.value = false
    bodyElement.classList.remove("dark-theme")
    bodyElement.classList.add("light-theme")
  } else {
    themeDark.value = true
    bodyElement.classList.remove("light-theme")
    bodyElement.classList.add("dark-theme")
  }
}
</script>

<style scoped>
button {
  background-color: var(--background-button-theme);
  color: var(--color-button-theme);

  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5em;

  border: none;
}
.icon {
  width: 2em;
  color: var(--color-button-theme);
}
</style>

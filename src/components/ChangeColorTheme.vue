<template>
  <button type="button" v-on:click="changeTheme">
    {{ themeLabel(themeDark) }}
  </button>
</template>

<script setup>
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

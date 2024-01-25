<template>
  <button type="button" v-on:click="changeTheme">
    <div ref="circleSwitchRef" class="circleSwitch circleSwitchLeft"></div>
    <SunIcon class="icon" />
    <MoonIcon class="icon" />
  </button>
</template>

<script setup>
import { MoonIcon } from "@heroicons/vue/24/outline"
import { SunIcon } from "@heroicons/vue/24/solid"
import { ref, onMounted } from "vue"

const circleSwitchRef = ref(null)
let circleSwitch

onMounted(() => {
  circleSwitch = circleSwitchRef.value
})

const bodyElement = document.body
const themeDark = ref(bodyElement.classList.contains("dark-theme"))

function changeTheme() {
  console.log(circleSwitch)
  if (themeDark.value === true) {
    themeDark.value = false
    bodyElement.classList.remove("dark-theme")
    bodyElement.classList.add("light-theme")
    circleSwitch.classList.remove("circleSwitchLeft")
    circleSwitch.classList.add("circleSwitchRight")
  } else {
    themeDark.value = true
    bodyElement.classList.remove("light-theme")
    bodyElement.classList.add("dark-theme")
    circleSwitch.classList.remove("circleSwitchRight")
    circleSwitch.classList.add("circleSwitchLeft")
  }
}
</script>

<style scoped>
.circleSwitch {
  position: absolute;
  top: 0.15em;
  left: 0.2em;

  height: 2.3em;
  width: 2.3em;
  border-radius: 50%;

  transition: 1s;
}
.circleSwitchLeft {
  background-color: #fff;
}
.circleSwitchRight {
  transform: translateX(3em);
  background-color: #000;
}
button {
  background-color: var(--background-button-theme);
  color: var(--color-button-theme);
  border: none;

  position: relative;
  padding: 0.3em;
  border-radius: 2em;

  display: flex;
  justify-content: center;
  align-items: center;
  gap: 1em;

  cursor: pointer;
}
.icon {
  width: 2em;
  color: var(--color-button-theme);
  transition: 1s;
}
</style>

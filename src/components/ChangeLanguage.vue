<template>
  <select
    title="Select Language"
    class="selectLanguage"
    v-on:change="setLocale"
    v-bind:value="t.locale.value"
  >
    <option value="en">English</option>
    <option value="pt">Portuguese</option>
  </select>
</template>

<script setup>
import { useI18n } from "vue-i18n"

const t = useI18n()

function setLocale(e) {
  t.locale.value = e.target.value
}
</script>

<style>
.selectLanguage {
  border: none;
  outline: none;
  font-family: Inter, Helvetica, Arial, sans-serif;
  color: var(--color-white-medium);
  background-color: var(--background-gray-medium);
}
</style>

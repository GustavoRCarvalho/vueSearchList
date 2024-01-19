<template>
  <select v-on:change="setLocale">
    {{
      locale
    }}
    <option value="en">English</option>
    <option value="pt">Portuguese</option>
  </select>
</template>

<script setup>
import { ref } from "vue"
import { useI18n } from "vue-i18n"

const t = useI18n()

const locale = ref(t.locale.value)

function setLocale(e) {
  t.locale.value = e.target.value
}
</script>

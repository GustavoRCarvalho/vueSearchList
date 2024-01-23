<template>
  <div class="container">
    <div class="buttonFilter">
      <span class="dropdownTitle">{{ $t("TypeFile") }}</span>
      <span class="dropdownSelect"
        >{{ $t("Book") }} <ChevronDownIcon class="arrowDown" />
      </span>
    </div>
    <div class="verticalLine"></div>
    <input class="inputSearch" :placeholder="$t('searchText')" type="text" />
    <button class="buttonSearch" type="button">{{ $t("searchButton") }}</button>
  </div>
</template>

<script setup>
import { ChevronDownIcon } from "@heroicons/vue/24/outline"
</script>

<style>
.container {
  background-color: var(--background-card);

  display: flex;
  align-items: center;

  padding-block: 1em;
  padding-inline: 1.3em;
  border-radius: 0.5em;
}
.inputSearch {
  font-family: Inter, Helvetica, Arial, sans-serif;
  border: none;
  outline: none;
  padding: 0;
  background-color: transparent;
  color: var(--color-title-item);

  width: 100%;
}
.buttonSearch {
  background-color: var(--background-button-search);
  color: var(--color-button-search);

  font-family: Inter, Helvetica, Arial, sans-serif;

  padding-block: 0.6em;
  padding-inline: 0.8em;
  height: min-content;

  border: none;
  border-radius: 2em;

  cursor: pointer;
}
.verticalLine {
  width: 1px;
  height: 2em;
  background-color: var(--color-item-description);
  margin-inline: 1em;
}
.buttonFilter {
  display: flex;
  flex-direction: column;
  white-space: nowrap;
  gap: 0.3em;

  justify-content: space-between;

  cursor: pointer;
}
.dropdownTitle {
  color: var(--color-list-title);
}
.dropdownSelect {
  color: var(--color-title-item);

  display: flex;
  justify-content: space-between;
  align-items: center;
}
.arrowDown {
  width: 1em;
}
</style>

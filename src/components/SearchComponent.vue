<template>
  <div class="container">
    <input class="inputSearch" placeholder="Search..." type="text" />
    <button class="buttonSearch" type="button">Search</button>
  </div>
</template>

<style>
.container {
  background-color: var(--background-gray-medium);

  display: flex;

  padding: 1em;
  border-radius: 0.5em;
}
.inputSearch {
  font-family: Inter, Helvetica, Arial, sans-serif;
  border: none;
  outline: none;
  padding: 0;
  background-color: transparent;
  color: var(--color-white-medium);

  width: 100%;
}
.buttonSearch {
  background-color: var(--background-red-dark);
  color: var(--color-red-medium);

  font-family: Inter, Helvetica, Arial, sans-serif;

  padding-block: 0.6em;
  padding-inline: 0.8em;

  border: none;
  border-radius: 2em;

  cursor: pointer;
}
</style>

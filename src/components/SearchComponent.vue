<template>
  <div class="container">
    <div class="buttonFilter">
      <span class="dropdownTitle">Type of File</span>
      <span class="dropdownSelect">Book -</span>
    </div>
    <div class="verticalLine"></div>
    <input class="inputSearch" placeholder="Search..." type="text" />
    <button class="buttonSearch" type="button">Search</button>
  </div>
</template>

<style>
.container {
  background-color: var(--background-gray-medium);

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
  color: var(--color-white-medium);

  width: 100%;
}
.buttonSearch {
  background-color: var(--background-red-dark);
  color: var(--color-red-medium);

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
  background-color: var(--color-gray-medium);
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
  color: var(--color-gray-light);
}
.dropdownSelect {
  color: var(--color-white-medium);
}
</style>

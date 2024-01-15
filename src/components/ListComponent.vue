<template>
  <div class="listComponentContainer">
    <h4 class="listTitle">Popular</h4>
    <ul class="listComponent">
      <slot></slot>
    </ul>
  </div>
</template>

<script>
export default {}
</script>

<style>
.listComponent {
  padding: 0;
  margin: 0;
}
.listComponentContainer {
  background-color: var(--background-gray-medium);

  padding: 1em;
  margin-top: 0.5em;

  border-radius: 0.5em;
}
.listTitle {
  color: var(--color-white-medium);

  padding: 0;
  margin: 0;
}
</style>

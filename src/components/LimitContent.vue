<template>
  <div class="limitContainer">
    <slot></slot>
  </div>
</template>

<style>
.limitContainer {
  width: 80%;
  @media (min-width: 1440px) {
    width: calc(1440px * 0.8);
  }
}
</style>

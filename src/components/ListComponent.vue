<template>
  <div class="listComponentContainer">
    <h4 class="listTitle">{{ $t("Popular") }}</h4>
    <ul class="listComponent">
      <slot></slot>
    </ul>
    <NotificationList />
  </div>
</template>

<script>
import NotificationList from "./NotificationList.vue"

export default { components: { NotificationList } }
</script>

<style>
.listComponent {
  padding: 0;
  margin: 0;
}
.listComponentContainer {
  background-color: var(--background-card);
  position: relative;

  padding: 1em;
  margin-top: 0.5em;

  border-radius: 0.5em;
}
.listTitle {
  color: var(--color-list-title);

  padding: 0;
  margin: 0;
}
</style>

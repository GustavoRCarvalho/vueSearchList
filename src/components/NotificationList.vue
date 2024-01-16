<template>
  <div class="notificationBlur">
    <button class="notificationButton">
      3 books just added <NotificationImage />
    </button>
  </div>
</template>

<script>
import NotificationImage from "./NotificationImage.vue"

export default {
  components: {
    NotificationImage,
  },
}
</script>

<style>
.notificationBlur {
  position: absolute;
  bottom: 0;
  left: 0;

  display: flex;
  align-items: flex-end;
  justify-content: center;

  backdrop-filter: blur(5px);

  padding-bottom: 1em;
  height: 6em;
  width: 100%;
}
.notificationButton {
  display: flex;
  align-items: center;
  background-color: var(--background-white-light);

  font-family: Inter, Helvetica, Arial, sans-serif;
  font-weight: bold;

  padding-block: 0.7em;
  padding-inline: 1.4em;

  border: none;
  border-radius: 5em;

  cursor: pointer;
}
</style>

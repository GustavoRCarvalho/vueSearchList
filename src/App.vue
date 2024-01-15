<template>
  <SearchComponent />
  <ListComponent>
    <template v-for="value in listItems" v-bind:key="value.title">
      <ListItemComponent
        :src="value.src"
        :title="value.title"
        :author="value.author"
        :category="value.category"
        :year="value.year"
        :pages="value.pages"
    /></template>
  </ListComponent>
</template>

<script>
import SearchComponent from "./components/SearchComponent.vue"
import ListComponent from "./components/ListComponent.vue"
import ListItemComponent from "./components/ListItemComponent.vue"

const listItems = [
  {
    src: "..\\assets\\images\\capaLivro.webp",
    title: "Title",
    author: "Author",
    category: "Category",
    year: "2023",
    pages: "000",
  },
  {
    src: "..\\assets\\images\\capaLivro.webp",
    title: "Title",
    author: "Author",
    category: "Category",
    year: "2023",
    pages: "000",
  },
]

export default {
  name: "App",
  components: {
    SearchComponent,
    ListItemComponent,
    ListComponent,
  },
  data() {
    return {
      listItems: listItems,
    }
  },
}
</script>

<style>
@font-face {
  font-family: Inter;
  src: url("~@/assets/fonts/Inter-Regular.ttf");
}
#app {
  font-family: Inter, Helvetica, Arial, sans-serif;
}
body {
  --background-gray-dark: #131313;
  --background-gray-medium: #1a1a1a;
  --background-gray-medium-light: #252525;
  --background-gray-light: #363636;
  --background-red-dark: #301f18;
  --color-white-medium: #e4e4e4;
  --color-red-medium: #dd5107;
  --color-gray-medium: #3f3f43;
  --color-gray-light: #797979;
  display: flex;
  align-items: center;
  justify-content: center;

  height: 100dvh;

  background-color: var(--background-gray-dark);
}
</style>

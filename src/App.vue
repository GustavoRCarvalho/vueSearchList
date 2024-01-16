<template>
  <LimitContent>
    <SearchComponent />
    <ListComponent>
      <template v-for="(value, index) in listItems" v-bind:key="value.title">
        <ListItemComponent
          v-if="showAllList(index)"
          :src="value.src"
          :title="value.title"
          :author="value.author"
          :category="value.category"
          :year="value.year"
          :pages="value.pages"
      /></template>
    </ListComponent>
  </LimitContent>
</template>

<script>
import SearchComponent from "./components/SearchComponent.vue"
import ListComponent from "./components/ListComponent.vue"
import ListItemComponent from "./components/ListItemComponent.vue"
import LimitContent from "./components/LimitContent.vue"
import capaLivro from "./assets/images/capaLivro.webp"
import capaLivro2 from "./assets/images/capaLivro2.webp"

const listItems = [
  {
    src: capaLivro,
    title: "Title",
    author: "Author",
    category: "Category",
    year: "2023",
    pages: "000",
  },
  {
    src: capaLivro2,
    title: "Title 2",
    author: "Author 2",
    category: "Category 2",
    year: "2023",
    pages: "111",
  },
  {
    src: capaLivro,
    title: "Title 3",
    author: "Author 3",
    category: "Category 3",
    year: "2023",
    pages: "222",
  },
  {
    src: capaLivro2,
    title: "Title 4",
    author: "Author 4",
    category: "Category 4",
    year: "2023",
    pages: "333",
  },
  {
    src: capaLivro,
    title: "Title 5",
    author: "Author 5",
    category: "Category 5",
    year: "2023",
    pages: "444",
  },
]

export default {
  name: "App",
  components: {
    SearchComponent,
    ListItemComponent,
    ListComponent,
    LimitContent,
  },
  data() {
    return {
      listItems: listItems,
    }
  },
  methods: {
    showAllList: (number) => number < 4,
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

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  width: 100%;
  height: 100%;
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

  min-height: 100dvh;
  min-width: 100dvw;
  margin: 0;

  background-color: var(--background-gray-dark);
}
</style>

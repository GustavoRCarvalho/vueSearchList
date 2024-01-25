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

<script setup>
import SearchComponent from "./SearchComponent.vue"
import ListComponent from "./ListComponent.vue"
import ListItemComponent from "./ListItemComponent.vue"
import LimitContent from "./LimitContent.vue"
import capaLivro from "../assets/images/capaLivro.jpg"
import capaLivro2 from "../assets/images/capaLivro2.jpg"

const listItems = [
  {
    src: capaLivro,
    title: "Title",
    author: "Author",
    category: "Category",
    year: 2023,
    pages: 0,
  },
  {
    src: capaLivro2,
    title: "Title 2",
    author: "Author 2",
    category: "Category 2",
    year: 2023,
    pages: 111,
  },
  {
    src: capaLivro,
    title: "Title 3",
    author: "Author 3",
    category: "Category 3",
    year: 2023,
    pages: 222,
  },
  {
    src: capaLivro2,
    title: "Title 4",
    author: "Author 4",
    category: "Category 4",
    year: 2023,
    pages: 333,
  },
  {
    src: capaLivro,
    title: "Title 5",
    author: "Author 5",
    category: "Category 5",
    year: 2023,
    pages: 444,
  },
]
const showAllList = (number) => number < 4
</script>

<script setup>
import CompositionAPI from "./components/CompositionAPI.vue";
import OptionsAPI from "./components/OptionsAPI.vue"
import ReactiveData from "./components/ReactiveData.vue";
import ClassBinding from "./components/ClassBinding.vue";
import ConditionalRendering from "./components/ConditionalRendering.vue";
import ListRendering from "./components/ListRendering.vue";
import EventHandling from "./components/EventHandling.vue";
import Whatchers from "./components/Whatchers.vue";
import CustomComponent from "./components/CustomComponent.vue";

import { ref } from "vue";
const textFontSize = ref(1);

const books = ref([
  {id: 1, title: "Dom Quixote", authorName: "Miguel de Cervantes"},
  {id: 2, title: "Os Miseráveis", authorName: "Victor Hugo"},
  {id: 3, title: "Meditações", authorName: "Marco Aurélio"},
]);
</script>

<template>
  <OptionsAPI />
  <hr>
  <CompositionAPI />
  <hr>
  <ReactiveData />
  <hr>
  <ClassBinding />
  <hr>
  <ConditionalRendering />
  <hr>
  <ListRendering />
  <hr>
  <EventHandling />
  <hr>
  <Whatchers />
  <hr>
  <h1>Componente customizado (props and emits)</h1>
  <CustomComponent 
  v-bind:style="{fontSize: textFontSize + 'em'}"
  @text-increment="textFontSize += 0.1"
  @text-decrement="textFontSize -= 0.1"
  v-for="book in books"
  :key="book.id"
  :title="book.title" 
  :authorName="book.authorName"/>
</template>

<style scoped>

</style>

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
  <CustomComponent title="Dom Quixote" author-name="Miguel de Cervantes"/>
</template>

<style scoped>

</style>

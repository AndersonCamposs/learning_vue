<script setup>
import { ref } from 'vue';
const persons = ref([
    {name: "Judith", age: 12},
    {name: "Rick", age: 45},
    {name: "Daryl", age: 47}
])
</script>

<template>
    <h1>Renderização de listas</h1>
    <ul v-for="(person, index) in persons">
        <li>{{ index }} - {{ person.name }}, {{ person.age }}</li>
    </ul>
</template>

<style scoped>
ul {
    list-style: none;
}
</style>
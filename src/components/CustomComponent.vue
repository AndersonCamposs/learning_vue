<script setup>
defineProps([
    "title",
    "authorName"
])

const emit = defineEmits([
    "text-increment",
    "text-decrement"
])
</script>

<template>
    <div class="container">
        <p>Título: {{ title }}</p>
        <p>Nome do Autor: {{ authorName }}</p>
        <button @click="() => emit('text-increment')">Aumentar fonte</button>
        <button @click="() => emit('text-decrement')">Diminuir fonte</button>
    </div>
</template>

<style scoped>
.container {
    border: 2px solid #000;
    border-radius: 8px;
    text-align: center;
    padding: 8px;
    margin-bottom: 20px
}

button {
    margin: 0 7px;
}
</style>
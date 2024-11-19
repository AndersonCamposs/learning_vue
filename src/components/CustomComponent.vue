<script setup>
defineProps([
    "title",
    "authorName"
])
</script>

<template>
    <div class="container">
        <p>Título: {{ title }}</p>
        <p>Nome do Autor: {{ authorName }}</p>
    </div>
</template>

<style scoped>
.container {
    border: 2px solid #000;
    border-radius: 8px;
    text-align: center;
}
</style>
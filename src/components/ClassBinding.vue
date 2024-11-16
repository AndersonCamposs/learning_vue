<script setup>
import { ref } from 'vue';
    const hasError = ref(false);

    const setClass = () => {
        hasError.value = !hasError.value;
    }
</script>

<template>
    <h1>Ligação de classe</h1>
    <h3 v-bind:class="{'text-danger': hasError}">Texto de exemplo</h3>
    <button v-on:click="setClass">Alterar a classe</button>
</template>

<style scoped>
.text-danger  {
    color: #d32525;
    font-weight:bold;
    font-style: italic;
}
</style>
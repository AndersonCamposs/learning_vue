<script setup>
import { computed, ref } from 'vue';

const count = ref(0);

function increment() {
    count.value++;
}

const getFlag = computed(() => {
    return (count.value % 2) === 0;
})
</script>
   
<template>
<h1>Renderização condicional</h1>
<button @click="increment">Incrementar</button>
<p v-if="getFlag">{{ count }} é par!</p>
<p v-else>{{ count }} é ímpar!</p>
</template>
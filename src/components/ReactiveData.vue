<script setup>
import { ref, reactive } from 'vue';
const refCount = ref(0);
const object = reactive({
    count: 0
})

function incrementRef() {
    refCount.value++;
}

function incrementReactive() {
    object.count++
}
</script>

<template>
<div class="container">
    <div>
        <h1>Usando Ref Object</h1>
        <button @click="incrementRef">Valor do Ref: {{ refCount }}</button>
    </div>
    <div>
        <h1>Usando Reactive Object</h1>
        <button @click="incrementReactive">Valor do object.count: {{ object.count }}</button>
    </div>
</div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
}

.container div {
    border-radius: 8px;
    border: 2px solid #000;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 10px;
    margin: 0 10px;
}
</style>
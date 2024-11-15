<script setup>
    import { ref, onMounted, onUpdated } from 'vue';

    const count = ref(0);

    function increment() {
        count.value++;
    }

    onMounted(() => {
        console.log("CompositionAPI\nO componente foi montado");
    })

    onUpdated(() => {
        console.log(`CompositionAPI\nO componente foi Re-Renderizado\nValor do contador: ${count.value}`)
    })

</script>

<template>
    <h1>Composition API</h1>
    <h3>{{ count }}</h3>
    <button v-on:click="increment">Incrementar</button>
</template>

<script>
export default {
    data() {
        return {
            count: 0
        }
    },

    methods: {
        increment() {
            this.count++
        }
    },

    mounted() {
        console.log(`OptionsAPI\nO componente foi montado`);
    }, 

    updated() {
        console.log(`OptionsAPI\nComponente Re-Renderizado\nValor do contador: ${this.count}`)
    }
}
</script>

<template>
    <h1>Options API</h1>
    <h3>{{ count }}</h3>
    <button v-on:click="increment">Incrementar</button>
</template>

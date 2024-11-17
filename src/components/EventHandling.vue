<script setup>
import { ref } from 'vue';

const name = ref('');

function sayHello() {
    alert(`Olá, ${name.value}`)
}

function showKey(e) {
    console.log(e.key);
}
</script>

<template>
    
    <h1>Manipulador de eventos</h1>
    <form>
        <label for="inputName">Seu nome</label>
        <input v-model="name" v-on:keydown="showKey" type="text" id="inputName">
        <button v-on:click.prevent="sayHello" type="submit">Enviar</button>
    </form>
</template>

<style scoped>
form {
    display: flex;
    flex-direction: column;
    align-items: center;
}

form > * {
    margin: 10px;
}

button {
    max-width: 10%;
}

input {
    border: 2px solid #000;
    border-radius: 8px;
    padding: 8px;
    font-size: 1.5em;
    max-width: 30%;
}
</style>
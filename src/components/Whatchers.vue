<script setup>
import { reactive, ref, watch } from 'vue';
const model = ref('');
const cep = ref('');
const data = reactive({});

watch(cep, async () => {
    try {
        let url = `https://viacep.com.br/ws/${cep.value}/json/`;

        const res = await fetch(url);
        const json = await res.json();

        if (json.erro === 'true') {
            throw new Error("Erro ao enviar a requisição");
        }

        data.localidade = json.localidade;
        data.uf = json.uf;
    } catch (e) {
        data.localidade = 0;
        data.uf = 0
    }
})
</script>

<template>
<h1>Observadores</h1>
<form @submit.prevent="() => cep = model">
    <label for="inputCep">Informe o seu CEP</label>
    <input v-model="model" type="text" id="inputCep">
    <button type="submit">Enviar</button>
    <p v-if="data.localidade && data.uf">Cidade: {{ `${data.localidade} - ${data.uf}` }}</p>
    <p v-else-if="data.localidade === 0 && data.uf === 0">Erro ao obter dados do cep informado</p>
</form>
</template>
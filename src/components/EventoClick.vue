<script setup>
import { ref } from "vue";

const mensagem = ref("Nenhum evento executado");

function eventoClick() {
    mensagem.value = "Evento executado!";
}
</script>

<template>
    <h2>Evento de Click</h2>
    <button @click="eventoClick">Clique Aqui</button>
    <p>{{ mensagem }}</p>
</template>
<style scoped>
h2 {
    color: #fff;
}
</style>

<script setup>
import { ref } from "vue";

const mensagem = ref("Nenhum evento executado");

function eventoClick() {
    mensagem.value = "Evento executado!";
}
</script>

<template>
    <button @click="eventoClick">Clique Aqui</button>
    <p>{{ mensagem }}</p>
</template>

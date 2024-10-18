<script setup>
import { ref } from "vue";

const texto = ref("");

// function eventoKeyDown(event) {
//     texto.value = event.key;
//     alert(`Tecla pressionada: ${event.key}`);
// }

function eventoKeyUp(event) {
    texto.value = event.key;
    alert(`Tecla pressionada: ${event.key}`);
}

function eventoKeyPress(event) {
    texto.value = event.key;
    alert(`Tecla pressionada: ${event.key}`);
}
</script>

<template>
    <h2>Evento de Teclado</h2>
    <input type="text" @keypress.b="eventoKeyPress" @keyup.a="eventoKeyUp" />
    <p>{{ texto }}</p>
</template>

<style scoped>
h2 {
    color: #fff;
}
</style>

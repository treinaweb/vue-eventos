<script setup>
import { ref } from "vue";

const textoFormulario = ref("nada foi enviado");
const textoPropagacao = ref("texto normal");

function eventoFormulario() {
    textoFormulario.value = "Informações enviadas";
}

function eventoDiv() {
    textoPropagacao.value = "Div Clicada!";
}

function eventoSpan() {
    textoPropagacao.value = "Span Clicado!";
}
</script>
<template>
    <h2>Propagação</h2>
    <form @submit.prevent="eventoFormulario">
        <input type="text" />
        <button type="submit">Enviar</button>
    </form>
    <p>{{ textoFormulario }}</p>

    <div @click="eventoDiv" class="div-evento">
        <span @click.stop="eventoSpan">{{ textoPropagacao }}</span>
    </div>
</template>
<style scoped>
.div-evento {
    background: rgb(13, 40, 13);
    padding: 1rem;
}

span {
    background: rgb(123, 73, 42);
}
</style>

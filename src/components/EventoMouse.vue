<script setup>
import { ref } from "vue";

const x = ref(0);
const y = ref(0);
const textoMouseEnter = ref("Nenhum evento disparado");

function eventoMouseEnter() {
    textoMouseEnter.value = "Mouse entrou na div!";
}

function eventoMouseLeave() {
    textoMouseEnter.value = "Mouse saiu da div!";
}

function eventoMouseMove(event) {
    x.value = event.clientX;
    y.value = event.clientY;
}
</script>

<template>
    <h2>Evento de Mouse</h2>
    <div @mouseleave="eventoMouseLeave" @mouseenter="eventoMouseEnter"></div>
    <p>{{ textoMouseEnter }}</p>
    <div @mousemove="eventoMouseMove"></div>
    <p>posição x:{{ x }}; y:{{ y }}</p>
</template>

<style scoped>
h2 {
    color: #fff;
}

div {
    background: #fff;
    height: 100px;
    border-radius: 10px;
}
</style>

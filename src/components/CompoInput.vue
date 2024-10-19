<script setup>
import { defineEmits, ref } from "vue";

const inputValue = ref("");

const emit = defineEmits(["inputEvento"]);

function emitirValor() {
    emit("inputEvento", inputValue.value);
}
</script>

<template>
    <div>
        <label for="nome">Nome: </label>
        <input type="text" v-model="inputValue" @input="emitirValor" />
    </div>
</template>

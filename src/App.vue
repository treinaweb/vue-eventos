<script setup>
import EventoClick from "./components/EventoClick.vue";
import EventoTeclado from "./components/EventoTeclado.vue";
</script>

<template>
    <div>
        <EventoClick />
    </div>

    <div>
        <EventoTeclado />
    </div>
</template>

<style scoped>
div {
    margin-bottom: 2rem;
}
</style>

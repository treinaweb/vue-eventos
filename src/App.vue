<script setup>
import EventoClick from "./components/EventoClick.vue";
import EventoTeclado from "./components/EventoTeclado.vue";
import EventoMouse from "./components/EventoMouse.vue";
</script>

<template>
    <div>
        <EventoClick />
    </div>
    <hr />
    <div>
        <EventoTeclado />
    </div>
    <hr />
    <div>
        <EventoMouse />
    </div>
</template>

<style scoped>
hr {
    margin: 2rem 0;
}
</style>

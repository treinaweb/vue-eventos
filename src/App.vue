<script setup>
import EventoClick from "./components/EventoClick.vue";
import EventoTeclado from "./components/EventoTeclado.vue";
import EventoMouse from "./components/EventoMouse.vue";
import Propagacao from "./components/Propagacao.vue";
import CampoInput from "./components/CompoInput.vue";

import { ref } from "vue";

const nome = ref("");

function capturarValor(valor) {
    nome.value = valor;
}
</script>

<template>
    <main>
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
        <hr />
        <div>
            <Propagacao />
        </div>
        <hr />
        <div>
            <h2>Emit</h2>
            <form>
                <CampoInput @inputEvento="capturarValor" />
            </form>
            <p>O seu nome é: {{ nome }}</p>
        </div>
    </main>
</template>

<style scoped>
h2 {
    color: #fff;
}
hr {
    margin: 2rem 0;
}

main {
    margin-bottom: 20rem;
}
</style>

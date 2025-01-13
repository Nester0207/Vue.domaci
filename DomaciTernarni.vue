<script setup>
import { ref } from "vue";

const nahodneCislo = ref(Math.random());
setInterval(() => {
    nahodneCislo.value = (Math.floor(Math.random() * 50));
}, 2500);
</script>

<template>
    <p>Padlo cislo: {{ nahodneCislo }}</p>
    <p>Cislo je: {{ (nahodneCislo%2) ? "Liche" : "Sude" }} </p>
    <p>Cislo je mensi nez 25: {{ (nahodneCislo < 25) ? "Ano" : "Ne" }}</p>
</template>
<script setup>

import { ref } from "vue"; 

const casovac = ref(10);
setInterval(() => {
    if (casovac.value > 0) {
        casovac.value -= 1;
    } else {
        casovac.value = "Hotovo";
    }
}, 1000);

</script>

<template>
    <h3>Domaci ukol</h3>
    <p>Cas ukolu:</p>
    <p>{{ casovac }}</p>
</template>

<style scoped>
</style>
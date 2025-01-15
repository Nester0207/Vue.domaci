<script setup>
import { ref } from "vue"

const prvniKostka = ref();
const druhaKostka = ref();

function hod() {
   prvniKostka.value = (Math.ceil(Math.random() * 6));
   druhaKostka.value = (Math.ceil(Math.random() * 6));
}
</script>

<template>
    <h3>Hod kostkami</h3>
    <button @click="hod">Hod kostkami</button>
    <p>Prvno kostka: {{ prvniKostka }}</p>
    <p>Druha kostka: {{ druhaKostka }}</p>
    <p>Vysledek: {{ (prvniKostka == druhaKostka) ? "Vyhrali jste" : "Hazejte znovu!" }}</p>
</template>
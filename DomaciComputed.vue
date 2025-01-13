<script setup>
import { ref, computed } from "vue"; 

const delka = ref(Math.floor(Math.random() * 100));
const sirka = ref(Math.floor(Math.random() * 100));

const obsah = computed(() => {
   let sumaObsahu = delka.value + sirka.value;
   return sumaObsahu;
});
</script>

<template>
    <p>Delka obdelniku je {{ delka }}, sirka je {{ sirka }}, a obsah je {{ obsah }}</p>
</template>
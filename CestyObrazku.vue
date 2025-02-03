<script setup>
import {ref} from "vue"

import cestaKBull from "@/assets/svg/bull.svg";
import cestaKCat from "@/assets/svg/cat.svg";
import cestaKDuck from "@/assets/svg/duck.svg";
import cestaKParrot from "@/assets/svg/parrot.svg";
import cestaKSheep from "@/assets/svg/sheep.svg";

const obrazek = [cestaKBull, cestaKCat, cestaKDuck, cestaKParrot, cestaKSheep];

const dynamickaCesta = ref(0);
function zobraziObrazek() {
    const randomObrazek = Math.floor(Math.random() * obrazek.length);
    dynamickaCesta.value = obrazek[randomObrazek];
}

</script>

<template>

    <button @click="zobraziObrazek">Zobrazit nahodny obrazek</button>
    <img :src="dynamickaCesta" alt="">

</template>

<style scoped>
img {
    width: 5rem;
}
</style>
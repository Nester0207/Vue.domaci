<script setup>
import { ref } from 'vue';

const cislo = ref(0);


</script>

<template>

    <button @click="cislo++" :disabled="cislo >= 10">{{ cislo }}</button>

</template>
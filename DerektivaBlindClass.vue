<script setup>
import { ref } from "vue"

const pocitadlo = ref(5);
const objektTrid = ref({
    velky: false
});

function spustPocitadlo() {
    if(pocitadlo.value > 0) {
        pocitadlo.value--;
    }else{
        objektTrid.value.velky = true;
        setTimeout(() => {
            objektTrid.value.velky = false;
            pocitadlo.value = 5;
        }, 3000);
    }
}
</script>

<template>
    <h3>Derektiva Blind Class</h3>
    <button @click="spustPocitadlo">{{ pocitadlo }}</button>
    <div class="kolecko" :class="objektTrid"></div>
</template>

<style scoped>
.kolecko {
    height: 5rem;
    width: 5rem;
    background-color: blue;
    border-radius: 50%;
    transition: 1s all ease-in-out;
}
.kolecko.velky {
        background-color: chartreuse;
        height: 10rem;
        width: 10rem;   
}
</style>
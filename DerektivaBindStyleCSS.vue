<script setup>
import {ref} from "vue"

const objektStyle = ref({
    borderRadius: "50%",
    backgroundColor: "magenta",
    height: "7rem",
    width: "7rem"
})

function zmenVelkost(argVyska, argSirka) {
    objektStyle.value.height = `${argVyska}rem`;
    objektStyle.value.width = `${argSirka}rem`;
}

function zmenBarvu() {
    let cervena = Math.floor(Math.random() * 256);
    let zelena = Math.floor(Math.random() * 256);
    let modra = Math.floor(Math.random() * 256);
    objektStyle.value.backgroundColor = "rgb(" + cervena + "," + zelena + "," + modra + ")";
}

</script>

<template>
    <h4>Derektiva v-bibd (style + CSS)</h4>
    <button @click="zmenVelkost(10,10)">Zmen velkost 1</button>
    <button @click="zmenVelkost(15,15)">Zmen velkost 2</button>
    <button @click="zmenVelkost(30,30)">Zmen velkost 3</button>
    <button @click="zmenBarvu()">Barva</button>
    <div style="width: 7rem; height: 7rem; background-color: pink;" v-bind:style="objektStyle"></div>
</template>

<style scoped>

    
</style>
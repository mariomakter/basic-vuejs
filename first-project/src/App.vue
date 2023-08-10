<template>
    <h1>{{ title }}</h1>
    <input type="text" ref="input">
    <button id="counter" @click="increment">{{ count }}</button>
</template>
<!-- ref state -->
<script setup>
import { ref, onMounted, nextTick } from 'vue';
let title = ref('New value');
let count = ref(0);
 const increment = async()=>{
    count.value++;

    //dom update  before state
    console.log(document.getElementById('counter').textContent);
    await nextTick();
    //dom is updated
    console.log(document.getElementById('counter').textContent);
}
const input = ref(null);
onMounted(()=>{
    input.value.focus()
    console.log("input.value");
})

</script>
<style>

</style>

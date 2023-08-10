<template>
    <h1>{{ title }}</h1>
    <input type="text" ref="input">
</template>
<!-- ref state -->
<script setup>
import { ref, onMounted } from 'vue';
let title = ref('New value');
const input = ref(null);
onMounted(()=>{
    input.value.focus()
    console.log("input.value");
})

</script>
<style>

</style>


<template>
  <div class="container">
    <div class="row">
      <div class="col">
       <h1>{{ course.name }} by using{{ title }}</h1>
       <button @click="increment(2)">+</button>
       <h3>{{ inc }}</h3>
       <button @click="decrement(1)">-</button>
      </div>
    </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import {ref, reactive} from 'vue';
let title = ref(' Function/method ');
const inc = ref(0);
inc.value += 1;
let course = reactive({
  name: 'vuejs',
  mentor:'Ibrahim Mahmud',
  platform:'Instructory'
});
function increment(amount){
  inc.value +=amount;
}
function decrement(amount){
  inc.value -=amount;
}
</script>


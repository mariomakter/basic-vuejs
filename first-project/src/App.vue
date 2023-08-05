<template>
  <div class="container">
    <div class="row">
      <div class="col">

  <h1 v-for="(todo,index) in todoList" :key="index">{{ index }}/{{ todo.todo }}</h1>
    </div>
  </div>
  <div class="">
    <img v-bind:src="imgurl" alt="">
  </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import {ref, reactive} from 'vue';
let title = ref(' Built in directives -  v-bind');
let showBtn = ref()
let todoList = ref([
{id:1, todo:'task1'},
{id:2, todo:'task2'},
{id:3, todo:'task3'},
]);
let imgurl = ref('https://picsum.photos/200');


</script>
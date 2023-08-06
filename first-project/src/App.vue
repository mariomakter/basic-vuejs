<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1 v-for="(todo, index) in todoList" :key="index">
          {{ index }}/{{ todo.todo }}
        </h1>
      </div>
    </div>
    <div class="row">
      <div class="col-12" width="100%">
        <div :class="isActive ? 'bg-primary' : 'bg-danger'" width="100%">
          <img v-bind:src="imgurl" alt="" />
        </div>
        <div class="static"
          :class="{'bg-primary':isActive, 'text-denger':hasError}">
          Lorem Ipsum is simply dummy text of the printing and
           typesetting industry. Lorem Ipsum has been the industry'
           s standard dummy text ever since the 1500s, when an unknown
           printer took a galley of type and scrambled it to make
        </div>
      </div>
    </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import { ref, reactive } from "vue";
let title = ref(" Built in directives -  v-bind");

let isActive = ref(true);
let hasError = ref(true);
let showBtn = ref();
let todoList = ref([
  { id: 1, todo: "task1" },
  { id: 2, todo: "task2" },
  { id: 3, todo: "task3" },
]);
let imgurl = ref("https://picsum.photos/200");
</script>
<style>
.bg-danger {
  background-color: #ee4444;
}
.bg-primary {
  background-color: chartreuse;
}
.static{
  margin-top: 30px;
  margin-left: 10px;
}
.text-denger{
  background-color: red;
  font-size: 20px;
}
</style>

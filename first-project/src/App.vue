<template>
  <div class="container">
    <div class="row">
      <div class="col">
       <h1 v-if="showBtn">{{ course.name }} by using<span v-text="title"></span></h1>
       <h1 v-else-if="!showBtn">{{ showBtn }}</h1>
       <h1 v-else>no thing happen</h1>
       <h2>couese by {{ fullName }}</h2>
      </div>
      <button @click="showBtn=!showBtn">show/hide</button>
    </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import {ref, reactive} from 'vue';
let title = ref(' Built in directives -  v-tex');
const count = ref(0);
let rawHtml = ref('<li>task1</li>');
let showBtn = ref()
let course = reactive({
  name: 'vuejs',
  mentor_firstName:'Ibrahim',
  mentor_lastName:'Mahmud',
  platform:'Instructory'
});

</script>
<template>
  <div class="container">
    <div class="row">
      <div class="col">
       <h1>{{ course.name }} by using<span v-text="title"></span></h1>
       <h1 v-html="rawHtml"></h1>
       <h2>couese by {{ fullName }}</h2>
      </div>
    </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import {ref, reactive} from 'vue';
let title = ref(' Built in directives -  v-tex');
const count = ref(0);
let rawHtml = ref('<li>task1</li>');
let course = reactive({
  name: 'vuejs',
  mentor_firstName:'Ibrahim',
  mentor_lastName:'Mahmud',
  platform:'Instructory'
});

</script>
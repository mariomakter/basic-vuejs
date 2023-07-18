
<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1>My name is {{ myName }}</h1>
        <h1>Name:{{ course.name }} </h1>
        <p>address:{{ course.address }} </p>
        <p>Course Name: {{ course.courseName }} </p>
        <input type="number" v-model="inc">
        <button @click="inc++">+</button>
        <h3>{{ inc }}</h3>
        <button @click="inc--">-</button>
      </div>
    </div>
  </div>
</template>
<!-- ref state -->
<script>
import {ref} from 'vue';
const inc = ref(0);
inc.value += 1;
</script>


<!-- reactive state example -->
<!-- <script>
import {reactive} from 'vue';
const user = reactive({
  name : 'Abdullah',
  age: 27,
  address:{
    city: 'colcheste',
    country:'England'

  }
});
console.log(user.name);
console.log(user.address.city);

user.age +=1;
user.address.city = 'london';
console.log(user.age);
</script> -->

<!-- ref and reactive state -->
<script setup>
import { reactive, ref } from 'vue';
let count = ref(0);
count.value = 10;

const myName = 'Maria';
let course = reactive({
  name: 'Mariom',
  address: 'Shewarapara',
  courseName: 'Vuejs 3'
})
const courseName = ref("Vue js");
const mentor = ref("Mariom");
</script>


<!-- <script>
export default{
  data(){
    return{
      courseName:"vu js",
      mentor:"Mariom",
      count:0
    }
  }
}
</script> -->
<!-- <script>
export default{
  setup(){
    const courseName = "vue js";
     const  mentor = "Mariom";
    let  count = 0;
    return{count, courseName, mentor}
  }
   }
</script> -->
<!-- <script>
import {ref} from 'vue';
export default{
  setup(){
    let count =ref(0);
  const courseName = ref("Vue js");
  const mentor = ref("Mariom");
  }
}
</script> -->

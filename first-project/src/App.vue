<template>
  <div class="container">
    <div class="row">
      <div class="col">
       <h1 @click="changeName">{{ course.name }} by using{{ title }}</h1>
       <h2>couese by {{ fullName }}</h2>
       <button @click="increment(2)">+</button>
       <h3>{{ count }}/{{ oddOrEven }}</h3>
       <button @click="decrement(1)">-</button>
      </div>
    </div>
  </div>
</template>
<!-- ref state -->
<script setup>
import {ref, reactive, computed, watch} from 'vue';
let title = ref(' Function/method ');
const count = ref(0);
let course = reactive({
  name: 'vuejs',
  mentor_firstName:'Ibrahim',
  mentor_lastName:'Mahmud',
  platform:'Instructory'
});

// es6 method using
const increment = amount => count.value += amount;
const decrement = amount => count.value -= amount;
const changeName = () => course.name = "Maria";
const fullName = computed(()=>{
return course.mentor_firstName+' '+course.mentor_lastName;
});
const oddOrEven = computed(()=>{
//  (count.value%2==0)? 'even': 'odd';
 return count.value%2==0 ? 'even': 'odd';

})
watch(()=>count.value,(newValue,oldValue)=>{
console.log('newvalue', newValue);
console.log('oldValue', oldValue);
if(newValue>10){
  alert("counter value is over than 10");
}
})
</script>
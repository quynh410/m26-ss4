<script setup>
import { ref } from "vue";
let count = ref(0);
const randomCount = ref(1);
const number = ref([]);
// khi dung ref ;
// để cập nhật lại gái trị thì bắt buộc phải truy cập vào value
// khi sử dụng thì không cần dùng value
const handleCount = () => {
  // câph nhật lại giá trị của count
  count.value++;
};
const hanldeRandom = () => {
  randomCount.value = Math.floor(Math.random() * 10);
};
const handlePush = () => {
  const random = Math.ceil(Math.random() * 10); 
//   number.value.push(random);  CACHS 1
  number.value = [...number.value, random] //CACH 2:
};
</script>
<template>
  <div>
    <h2>Count: {{ count }}</h2>
    <button @click="handleCount">Count</button>
    <h2>Random Count: {{ randomCount }}</h2>
    <!-- <button @click="randomCount = Math.floor(Math.random() * 10)">Random Count</button> -->
    <button @click="hanldeRandom">Random</button>
    <!--  -->
    <h2>Push number : {{number}}</h2>
    <button @click="handlePush">Push number </button>
  </div>
</template>

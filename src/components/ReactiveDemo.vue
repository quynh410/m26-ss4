<script setup>
import { reactive } from "vue";

const userInfo = reactive({
  id: 1,
  userName: "Nguyen Van A",
});
const handleIncreaseId = ()=>{
    userInfo.id++;
    console.log(userInfo.id); 
  
}
</script>
<template>
  <div>
    <h2>Reacttive</h2>
    <p>ID: {{ userInfo.id }}</p>
    <p>Name: {{ userInfo.userName }}</p>
    <button @click="handleIncreaseId">Increase id</button>
  </div>
</template>

<style></style>


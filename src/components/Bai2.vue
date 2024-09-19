<script setup>
import { reactive } from "vue";

const com = reactive({
  company: "Rikkei Academy ",
  age: 2,
});
const handelChangeData = () => {
  com.company = "Rikkei Education";
  com.age = 1;
};
</script>

<template>
  <div>
    <br />
    <b>Company : {{ com.company }}</b>
    <b>Age : {{ com.age }}</b> <br />
    <button @click="handelChangeData">Change Data</button>
  </div>
</template>

<style></style>

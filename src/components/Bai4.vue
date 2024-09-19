<script setup>
import { ref, watch } from "vue";
const inputValue = ref("");
watch(inputValue, (newValue, oldValue) => {
  console.log(`Giá trị thay đổi từ "${oldValue}" thành "${newValue}"`);
});
</script>

<template>
  <div>
    <br>
    <input v-model="inputValue" placeholder="Enter something..." />
  </div>
</template>

<style></style>

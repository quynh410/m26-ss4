<script setup>
import { ref, watch } from "vue";

    const count = ref(0);
    const handleCount = ()=>{
       count.value++;
    }
    watch(count, (newValue, oldValue)=>{
        // lang ghe su thay doi cua count
        console.log(`Count changed from ${oldValue} to ${newValue}`);
    })
</script>

<template>
  <h2>Count: {{count}}</h2>
  <button @click="handleCount">Click</button>
</template>

<style>

</style>
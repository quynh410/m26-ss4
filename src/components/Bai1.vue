<script setup>
import { ref } from "vue"

    const count = ref(0);
    const handleCount = () => {
        count.value++;
    };
</script>
<template>
    <button @click="handleCount">Click{{ count }} lan</button>
</template>


<style>

</style>
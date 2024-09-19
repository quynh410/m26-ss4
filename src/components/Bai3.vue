<script setup>
import { ref, computed } from "vue";

const width = ref(10);
const height = ref(20);

const area = computed(() => width.value * height.value);

const increaseWidth = () => {
  width.value += 10;
};
</script>

<template>
  <div>
    <p>Area: {{ area }}</p>

    <button @click="increaseWidth">Increase width</button>
  </div>
</template>

<style></style>

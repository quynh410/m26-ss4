<script setup>
import { ref } from 'vue';
const totalCartPrice = ref(0);
const inputPrice = ref(0);
const addToCart = () => {
  totalCartPrice.value += Number(inputPrice.value);
  inputPrice.value = 0; 
};
</script>

<template>
  <div>
    <input type="number" v-model="inputPrice" />
    <button @click="addToCart">Add to cart</button>
        <p>Tổng tiền trong giỏ hàng: {{ totalCartPrice }}</p>
  </div>
</template>

<style>
</style>

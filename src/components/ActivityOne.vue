<script setup>
import { ref } from "vue";
//  const ✅
//  let ✅
// @click ✅
// function ✅
let number = ref(0);

function increment(num) {
  number.value += num;
}

function decrement(num) {
  number.value -= num;
}

</script>

<template>
  <div class="number">{{ number }}</div>
  <div class="wrapper">
    <button @click="increment(1)">Increment by 1</button>
    <button @click="decrement(1)">Decrement by 1</button>

    <button @click="increment(2)">Increment by 2</button>
    <button @click="decrement(2)">Decrement by 2</button>

    <button @click="increment(3)">Increment by 3</button>
    <button @click="decrement(3)">Decrement by 3</button>

    <button @click="increment(4)">Increment by 4</button>
    <button @click="decrement(4)">Decrement by 4</button>
  </div>
</template>

<style>
.number {
  color: white;
  font-size: 50px;
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
  padding: 10px;
  background-color: green;
}

.wrapper {
  display: flex;
  grid-gap: 40px;
}
</style>

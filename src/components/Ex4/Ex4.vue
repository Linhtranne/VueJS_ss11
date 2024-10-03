<template>
  <div>
    <h1>Bài 4</h1>
    <h1>Parent Component</h1>
    <h2>Age: {{ age }}</h2>
    <button @click="increaseAge">Increase Age</button>
    <Child :age="age" />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Child from './Child.vue';
const age = ref(1);

const increaseAge = () => {
  age.value += 1;
};
</script>

<style scoped>
</style>

<template>
  <div>
    <h1>Bài 9</h1>
    <h1>Ứng dụng đếm số: {{ count }}</h1>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const count = ref(0);

onMounted(() => {
  console.log("Ex9:Component mounted");
  
  const interval = setInterval(() => {
    count.value++;
  }, 1000);

  onUnmounted(() => {
    clearInterval(interval);
  });
});
</script>

<style scoped>
h1 {
  font-family: Arial, sans-serif;
  color: #333;
}
</style>

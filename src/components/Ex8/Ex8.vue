<template>
  <div>
    <h1>
      Bài 8
    </h1>
   <p>Page width :{{width}}</p>
  </div>
</template>

<script setup>
import { onMounted, onUpdated, ref } from 'vue';
const width = ref(window.innerWidth);
onUpdated(() => {
  width.value = window.innerWidth;
});

onMounted(() => {
  console.log("Ex8:Component is now mounted");
  
});
</script>

<style scoped>
</style>

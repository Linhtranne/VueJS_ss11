<template>
    <div>
      <p>Received Age: {{ age }}</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps,  onMounted, onUpdated } from 'vue';
  const props = defineProps({
    age: {
      type: Number,
      required: true
    }
  });
  onUpdated(()=>{
    alert ("Giá trị biến age đã được thay đổi")
  }
)
  onMounted(() => {
    console.log('Ex4:Component is mounted');
  });
  </script>
  
  <style scoped>
  </style>
  
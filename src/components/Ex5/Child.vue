<template>
    <div>
      <h2>Child Component</h2>
    </div>
  </template>
  
  <script setup>
  import { onBeforeUnmount, onUnmounted } from 'vue';
  
  onBeforeUnmount(() => {
    console.log('Ex5:beforeUnmount: Component is about to be unmounted');
  });
  
  onUnmounted(() => {
    console.log('Ex5:unmounted: Component has been unmounted');
  });
  </script>
  
  <style scoped>
  </style>
  
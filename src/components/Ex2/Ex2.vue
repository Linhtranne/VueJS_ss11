<template>
  <div>
    <h1>Bài 2</h1>
    <h1>Counter: {{ count }}</h1>
    <button @click="increment">Counter</button>
  </div>
</template>

<script setup>
import { ref,  onMounted, onUpdated } from "vue";

const count = ref(0);
const increment = () => {
  count.value += 1;
};
onUpdated(()=> {
    console.log("Dữ liệu đã thay đổi.");
  });
onMounted(() => {
  console.log("Ex2:Component mounted.");
});

</script>

<style scoped></style>
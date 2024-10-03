<template>
  <div>
    <h1>Bài 3</h1>
    <p>Age: {{ age }}</p>
    <p>Company: {{ currentCompany }}</p>
    <button @click="randomizeAge">Random</button>
  </div>
</template>

<script>
  import { onMounted } from 'vue';
export default {

  data() {
    return {
      age: 1,
      companies: ["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"],
    };
  },
  computed: {
    currentCompany() {
      return this.companies[(this.age - 1) % this.companies.length];
    },
  },
  methods: {
    randomizeAge() {
      this.age = Math.floor(Math.random() * 10) + 1;
    },
    
  },
};
onMounted(() => {
    console.log('Ex3:Component is mounted');
  });
</script>

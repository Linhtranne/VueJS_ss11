<template>
  <div>
    <h1>Bài 7</h1>
    <input v-model="title" placeholder="Enter tab title" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "",
    };
  },
  watch: {
    title(newTitle) {
      document.title = newTitle || "Default Tab Title";
    },
  },
  mounted() {
    document.title = this.title;
  },
};
</script>

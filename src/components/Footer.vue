<script setup>
import { ref } from "vue";
const year = ref(new Date().getFullYear());
const href = ref("https://scrimba.com");
year.value = 2025;
</script>

<template>
  <footer>
    Created by <span><a :href>Professor Pickle</a></span> &copy;
    {{ year }}
  </footer>
</template>

<style scoped>
footer {
  position: fixed;
  margin: 0 auto;
  bottom: 0;
  text-align: center;
  color: #ccd6d9;
  padding-bottom: 20px;
}

footer span {
  font-family: cursive;
}
</style>

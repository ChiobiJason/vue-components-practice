<script setup>
import { ref } from "vue";
const quote = ref("First, solve the problem. Then, write the code.");
const author = ref("John Johnson");
const authorLink = ref("https://en.wikipedia.org/wiki/Steve_Jobs");
const isButtonDisabled = ref(true);

quote.value = "The only way to do great work is to love what you do.";
author.value = "Steve Jobs";
</script>

<template>
  <main>
    <section>
      <p>{{ quote }}</p>
      <span
        ><a :href="authorLink">{{ author }}</a></span
      >
    </section>
    <div id="buttons">
      <button :disabled="isButtonDisabled">Another!</button>
      <button :disabled="isButtonDisabled">Share</button>
    </div>
  </main>
</template>

<style scoped>
main {
  background: #ccd6d9;
  max-width: 90%;
  border-radius: 0 15px 0 15px;
  padding: 35px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

main section {
  display: flex;
  width: 100%;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 25px;
}

main p {
  font-weight: bold;
  font-style: italic;
  font-size: 2rem;
  text-align: left;
}

main p::before {
  content: '"';
}

main p::after {
  content: '"';
}

main span {
  align-self: end;
  color: #406473;
}

main span::before {
  content: "- ";
}

main button {
  background: #406473;
  color: white;
  padding: 10px;
  border: 0;
  font-size: 1.2rem;
  border-radius: 0 5px 0 5px;
  font-weight: bold;
  margin-top: 20px;
  cursor: pointer;
  transition: transform 0.2s;
}
main button:hover {
  transform: scale(1.05);
}

#buttons {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 30px;
}

button:disabled {
  background: grey;
  cursor: not-allowed;
  opacity: 0.5;
}
</style>

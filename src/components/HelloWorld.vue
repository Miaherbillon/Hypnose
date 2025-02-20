<script setup>
import { ref } from "vue";
import fontImage from "/src/assets/Font.png";
</script>

<template>
  <h1 class="title">M'Hypnose</h1>
</template>

<style scoped>
.title {
  width: 60%;
  margin: 2em auto;
  padding: 1.5em;
  border-radius: 50em;
  color: #000000;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: white;
  box-sizing: border-box;
  text-align: center;
}
h1 {
  box-sizing: border-box;
  border: 0.3em solid white;
  border-radius: 50%;
  overflow: hidden;
  font-size: 3em;
  text-align: center;
  box-shadow: 0 0.3em 1em rgba(0, 0, 0, 0.6);
  transform: translateY(0px);
  animation: float 6s ease-in-out infinite;
}

/* 📱 Responsive pour téléphones */
@media (max-width: 768px) {
  .title {
    width: 80%;
    padding: 1em 3em;
    border-radius: 5em;
  }

  h1 {
    font-size: 2em;
    border-width: 0.2em;
  }
}
</style>

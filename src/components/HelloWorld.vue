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
  margin: 4vw auto;
  padding: 5vh;
  border-radius: 50vh;
  color: #000000;
  display: flex;
  justify-content: center;
  background-color: white;
  box-sizing: border-box;
}
h1 {
  box-sizing: border-box;
  border: 5px white solid;
  border-radius: 50%;
  overflow: hidden;
  font-size: 3em;
  box-shadow: 0 5px 15px 0px rgba(0, 0, 0, 0.6);
  transform: translatey(0px);
  animation: float 6s ease-in-out infinite;
}
</style>

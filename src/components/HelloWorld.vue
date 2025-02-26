<script setup>
import { ref } from "vue";
import fontImage from "/src/assets/Font.png";
</script>

<template>
  <h1 class="title">M'Hypnose</h1>
  <FontAwesomeIcon icon="fa-solid fa-arrow-down-long" beat />
</template>

<style scoped>
.title {
  /* font-family: "Rubik Gemstones", serif; */
  /* font-family: "Fredericka the Great", serif; */
  font-family: "Yuji Syuku", serif;
  width: 60%;
  margin: 1em auto;
  padding: 0.5em;
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
  font-size: 4em;
  text-align: center;
  box-shadow: 0 0.3em 1em rgba(0, 0, 0, 0.6);
}

/* 📱 Responsive pour téléphones */
@media (max-width: 768px) {
  .title {
    font-family: "Poiret One", serif;

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

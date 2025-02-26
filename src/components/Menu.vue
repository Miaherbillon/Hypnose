<script setup>
import { ref } from "vue";
</script>

<template>
  <div>
    <a href="#contact">CONTACTEZ-MOI</a>
    <a href="#reservation">RESERVATION</a>
  </div>
</template>

<style scoped>
div {
  display: flex;
  justify-content: center;
  margin: auto;
  gap: 2em;
}
a {
  text-decoration: none;
  color: rgb(135, 89, 210);
}
@media (max-width: 880px) {
  a {
    font-size: 0.7em;
    color: rgb(135, 89, 210);
  }
}
</style>

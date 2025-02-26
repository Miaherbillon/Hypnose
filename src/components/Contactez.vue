<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="contact-container">
    <h4 id="contact">Une question ? Besoin d'informations ?</h4>
    <p>👋 N’hésitez pas à m’écrire, je vous répondrai avec plaisir !</p>
    <a href="mailto:mhypnose25@gmail.com" class="contact-button">
      ✉️ Cliquez ici pour m'envoyer un mail
    </a>
  </div>
</template>

<style scoped>
.contact-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin: 2em;
}

h4 {
  /* color: rgb(135, 89, 210); */
  font-size: 1.3em;
}

p {
  font-size: 1.1em;
  margin-bottom: 1.2em;
}

.contact-button {
  display: inline-block;
  background-color: rgba(135, 89, 210, 0.623);
  color: white;
  font-size: 1.2em;
  font-weight: bold;
  padding: 0.8em 1.2em;
  border-radius: 30px;
  text-decoration: none;
  transition: background-color 0.3s ease-in-out, transform 0.2s ease-in-out;
}

.contact-button:hover {
  color: rgb(255, 255, 255);
  transform: scale(1.05);
}
@media (max-width: 768px) {
  h4 {
    font-size: 1em;
  }
  p {
    font-size: 0.8em;
  }
  .contact-button {
    font-size: 0.8em;
    font-weight: bold;
    padding: 0.5em 1em;
  }
}
</style>

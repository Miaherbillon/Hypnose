<script setup>
import { ref } from "vue";
</script>

<template>
  <footer class="footer">
    <p>
      &copy; 2024 Mia Herbillon - Fondatrice de M'hypnose - Tous droits
      réservés.
    </p>
  </footer>
</template>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  font-size: 0.8em;
  color: #555; /* Une couleur légèrement plus douce pour améliorer l'aspect visuel */
}

@media (max-width: 768px) {
  .footer {
    width: 60%;
    margin: auto;
    text-align: center;
    font-size: 0.6em; /* Augmenter légèrement la taille du texte pour une meilleure lisibilité */
  }
}
</style>

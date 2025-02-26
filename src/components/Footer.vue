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
}
@media (max-width: 768px) {
  .footer {
    font-size: 0.5em;
  }
}
</style>

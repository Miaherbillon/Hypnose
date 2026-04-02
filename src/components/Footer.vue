<script setup>
// Simple footer statique
</script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <p>
        &copy; 2025 <strong>Mia Herbillon</strong> — Fondatrice de
        <strong>M'Hypnose</strong> — Tous droits réservés.
      </p>
      <p class="mentions">Besançon & Visio</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 40px 20px; /* Espace après le dernier bloc */
  font-family: "Quicksand", sans-serif;
}

.footer-content {
  text-align: center;
  color: #888;
  font-size: 0.85em;
  line-height: 1.5;
}

strong {
  color: #9d80cb;
  font-weight: 500;
}

.mentions {
  font-size: 0.9em;
  margin-top: 5px;
  letter-spacing: 1px;
  text-transform: uppercase;
  opacity: 0.7;
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .footer {
    padding: 30px 10px;
  }

  .footer-content {
    font-size: 0.75em; /* Plus lisible que 0.6em */
    width: 90%; /* On utilise plus d'espace sur mobile */
    margin: auto;
  }
}
</style>

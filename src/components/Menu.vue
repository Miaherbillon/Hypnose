<script setup>
// Navigation fluide vers les ancres ID de la page
</script>

<template>
  <nav class="nav-container">
    <a href="#votre-lien-de-rdv" class="nav-link">RÉSERVATION</a>
    <span class="separator">•</span>
    <a href="#contact" class="nav-link">CONTACT</a>
  </nav>
</template>

<style scoped>
.nav-container {
  display: flex;
  justify-content: center; /* Centré pour l'équilibre visuel */
  align-items: center;
  gap: 10px;
  padding: 10px 0;
  /* margin: 0 auto 10px auto; */
}

.nav-link {
  text-decoration: none;
  color: #777;
  font-family: "Quicksand", sans-serif;
  font-weight: 600; /* Un peu plus épais pour le côté pro */
  font-size: 0.85em;
  letter-spacing: 1.5px;
  padding: 8px 10px;
  border-radius: 50px; /* Effet pilule */
  transition: all 0.4s cubic-bezier(0.16, 1, 0.3, 1);
  background: rgba(255, 255, 255, 0); /* Fond invisible par défaut */
  border: 1px solid transparent;
}

/* Effet au survol : fond doux et changement de couleur */
.nav-link:hover {
  color: #9d80cb;
  background: rgba(157, 128, 203, 0.08); /* Un voile mauve très léger */
  border: 1px solid rgba(157, 128, 203, 0.15);
  transform: translateY(-2px);
}

/* Le séparateur devient une barre verticale élégante */
.separator {
  width: 1px;
  height: 10px;
  background-color: rgba(135, 89, 210, 0.2);
  margin: 0 5px;
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .nav-container {
    gap: 5px;
    padding: 10px 0;
  }

  .nav-link {
    font-size: 0.75em;
    padding: 6px 12px;
    letter-spacing: 1px;
    color: #9d80cb; /* Mauve direct sur mobile pour la clarté */
    background: rgba(157, 128, 203, 0.05); /* Petit fond constant sur mobile */
    border: 1px solid rgba(157, 128, 203, 0.1);
  }

  .separator {
    display: none; /* On épure au maximum sur mobile */
  }
}
</style>

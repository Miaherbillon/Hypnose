<script setup>
// L'image fontImage n'est pas utilisée dans ton template,
// je l'enlève pour nettoyer le code.
</script>

<template>
  <div class="title-wrapper">
    <h1 class="main-title">M'Hypnose</h1>
    <div class="icon-container">
      <FontAwesomeIcon
        icon="fa-solid fa-arrow-down-long"
        beat
        class="arrow-icon" />
    </div>
  </div>
</template>

<style scoped>
.title-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  /* margin: 2em auto; */
  width: 100%;
}

.main-title {
  /* On utilise Playfair pour le côté premium/bien-être */
  font-family: "Playfair Display", serif;
  font-size: 3.5em;
  color: #444;

  /* Structure de la "bulle" */
  background-color: white;
  padding: 0.2em 1.5em;
  border-radius: 100px; /* Effet pillule plutôt que cercle parfait */

  /* Ombre très douce pour rester zen */
  box-shadow: 0 10px 30px rgba(157, 128, 203, 0.15);

  border: 4px solid white;
  text-align: center;
  transition: all 0.3s ease;
}

.icon-container {
  margin-top: 1.5em;
}

.arrow-icon {
  color: #9d80cb;
  font-size: 1.5em;
}

/* RESPONSIVE CIBLÉ : SUPPRESSION DES ESPACES */
@media (max-width: 768px) {
  .container {
    padding: 10px;
  }

  /* 1. On rapproche le titre M'Hypnose du haut de l'écran */
  header.hero-section {
    margin-top: 5px; /* On réduit l'espace avant le header */
  }

  /* 2. On réduit la bulle blanche elle-même */
  .title-wrapper h1 {
    font-size: 2em !important;
    padding: 0.4em 20%; /* Réduction drastique du vide interne */
    margin: 0 !important; /* On annule les marges autour du titre */
    border-radius: 25px; /* Arrondi plus adapté à la petite taille */
  }

  /* 3. On réduit l'espace vertical entre la pillule et le texte */
  .typed-container {
    /* C'est ce min-height qui crée le grand vide. On le casse. */
    min-height: auto !important;
    margin-top: 15px !important; /* C'est tout l'espace qu'il faut */
    padding: 0 10px !important;
  }

  /* 4. On adapte le texte de la machine à écrire */
  .typed-heading {
    font-size: 1.05em !important;
    line-height: 1.3 !important;
    color: #888;
  }

  /* 5. Flèche et autres éléments */
  .icon-container {
    margin-top: 5px !important;
  }
}
</style>

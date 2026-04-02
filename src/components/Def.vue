<script setup>
// Texte statique pour l'explication des méthodes
</script>

<template>
  <section class="definition-container">
    <div class="definition-card">
      <h2 class="section-title">
        Elmanienne ou Ericksonienne : Quelle différence ?
      </h2>

      <p>
        L’<strong>hypnose Elmanienne</strong>, développée par Dave Elman, est la
        méthode que je privilégie à <strong>Besançon</strong>. C'est une
        approche <strong>rapide et structurée</strong> permettant d’atteindre un
        état hypnotique profond en quelques minutes grâce à des inductions
        rapides et des <strong>suggestions directes</strong>.
      </p>

      <p class="comparison-text">
        À l'inverse, l’hypnose Ericksonienne repose sur une approche plus
        <em>subtile et indirecte</em>. Elle utilise des métaphores pour guider
        l’inconscient de manière plus progressive.
      </p>

      <p class="final-note">
        L’<strong>hypnose Elmanienne (OMNI)</strong> est donc idéale pour des
        transformations <strong>rapides et efficaces</strong>. C'est cette
        précision que je vous propose de découvrir en séance.
      </p>
    </div>
  </section>
</template>

<style scoped>
/* Conteneur extérieur */
.definition-container {
  padding: 0;
  max-width: 1000px;
  margin: 30px auto;
}

/* La carte avec l'effet de verre harmonisé */
.definition-card {
  font-family: "Quicksand", sans-serif;
  background: #ffffffa5; /* Même transparence que les autres cartes */
  padding: 35px 25px;
  border-radius: 40px;
  box-shadow: 0 15px 35px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
  color: #6c6767;
  line-height: 1.7;
  text-align: center; /* Harmonisé avec le reste du site */
}

/* Titre H2 (Identique aux autres sections) */
.section-title {
  font-family: "Playfair Display", serif;
  font-size: 1.8em;
  color: #444;
  margin-bottom: 25px;
  line-height: 1.2;
}

/* Texte de comparaison plus discret */
.comparison-text {
  font-size: 0.95em;
  color: #888;
  border-top: 1px solid rgba(157, 128, 203, 0.1);
  padding-top: 20px;
  margin-top: 20px;
}

.final-note {
  margin-top: 20px;
  font-weight: 500;
}

strong {
  color: #9d80cb;
  font-weight: 700;
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .definition-card {
    padding: 25px 15px;
    border-radius: 30px;
    /* On remonte la taille à 0.9em pour la lisibilité mobile */
    font-size: 0.9em;
  }

  .section-title {
    font-size: 1.4em !important;
    margin-bottom: 15px;
  }

  .definition-container {
    padding: 0 10px;
  }
}
</style>

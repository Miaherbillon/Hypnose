<script setup>
// Pas besoin de ref ici car le texte est statique
</script>

<template>
  <section class="definition-container">
    <div class="definition-card">
      <h2 class="title">Elmanienne ou Ericksonienne : Quelle différence ?</h2>

      <p>
        L’<strong>hypnose Elmanienne</strong>, développée par Dave Elman, est la
        méthode que je privilégie à <strong>Besançon</strong>. C'est une
        approche <strong>rapide et structurée</strong> permettant d’atteindre un
        état hypnotique profond en quelques minutes grâce à des inductions
        rapides et des <strong>suggestions directes</strong>.
      </p>

      <!-- <div class="highlight-box">
        <p>
          Elle est particulièrement adaptée à l'accompagnement thérapeutique
          concret :
          <strong>gestion de la douleur, phobies ou sevrage tabagique</strong>.
        </p>
      </div> -->

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
.definition-container {
  padding: 20px;
  max-width: 900px;
  margin: auto;
}

.definition-card {
  font-family: "Quicksand", sans-serif;
  background: #ffffffa5;
  padding: 40px;
  border-radius: 30px;
  box-shadow: 0 15px 35px rgba(155, 107, 195, 0.05);
  border: 1px solid rgba(155, 107, 195, 0.1);
  color: #6c6767;
  line-height: 1.7;
}

.title {
  font-family: "Playfair Display", serif;
  color: #444;
  text-align: center;
  font-size: 1.8em;
  margin-bottom: 25px;
}

.highlight-box {
  background-color: #fcfaff;
  padding: 20px;
  border-left: 4px solid #9d80cb;
  margin: 25px 0;
  border-radius: 0 15px 15px 0;
  font-style: italic;
}

.comparison-text {
  font-size: 0.95em;
  color: #888;
  border-top: 1px solid #f0f0f0;
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

/* RESPONSIVE */
@media (max-width: 768px) {
  .definition-card {
    font-size: 0.7em;
    padding: 25px 20px;
    border-radius: 25px;
    text-align: left; /* Plus lisible sur petit écran que le 'justify' */
  }

  .title {
    font-size: 1.4em;
    line-height: 1.3;
  }

  .definition-container {
    padding: 10px;
  }
}
</style>

<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="definition">
    <h2 class="title">
      Hypnose Elmanienne ou Ericksonienne : Quelle différence ?
    </h2>

    <p id="info">
      L’<strong>hypnose Elmanienne</strong>, développée par Dave Elman, est la
      méthode que je privilégie à <strong>Besançon</strong>. C'est une approche
      <strong>rapide et structurée</strong> permettant d’atteindre un état
      hypnotique profond en quelques minutes grâce à des inductions rapides et
      <strong>des suggestions directes</strong>.
    </p>

    <p class="highlight-box">
      <strong>
        Elle est particulièrement efficace en hypnose thérapeutique, notamment
        pour la gestion de la douleur, les phobies ou le sevrage tabagique.
      </strong>
    </p>

    <p>
      En opposition, l’hypnose Ericksonienne, créée par Milton Erickson, repose
      sur une approche plus <strong>subtile et indirecte</strong>. Elle utilise
      des métaphores et des suggestions ouvertes pour guider l’inconscient de
      manière plus douce et progressive.
    </p>

    <p>
      L’<strong>hypnose Elmanienne</strong> est donc idéale pour des
      transformations <strong>rapides et efficaces</strong>. C'est cette
      efficacité que je vous propose de découvrir lors de nos séances d'<strong
        >hypnose à Besançon</strong
      >
      ou en ligne.
    </p>
  </div>
</template>

<style scoped>
/* Conteneur principal */
.definition {
  font-family: "Yuji Syuku", serif;
  width: 80%;
  max-width: 800px;
  padding: 3vh 4vw;
  margin: 4vh auto;
  /* border: 1px solid rgba(135, 89, 210, 0.2); */
  background: #ffffffa5;
  border-radius: 15px;
  box-shadow: 0 20px 50px rgba(135, 89, 210, 0.12);
  line-height: 1.8; /* Aéré pour la lecture */
  text-align: justify;
  color: #6c6767;
}

/* Titre passé en H2 */
.title {
  color: #9d80cb;
  text-align: center;
  font-size: 1.8em;
  margin-bottom: 3vh;
  font-weight: bold;
}

/* Bloc de mise en avant */
.highlight-box {
  background-color: rgba(135, 89, 210, 0.05);
  padding: 15px;
  border-left: 4px solid #9d80cb;
  margin: 20px 0;
}

strong {
  color: #9d80cb;
}

@media (max-width: 880px) {
  .definition {
    width: 95%;
    font-size: 0.95em;
    padding: 20px;
  }
  .title {
    font-size: 1.4em;
  }
}
</style>

<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="definition">
    <h1 class="title">L'Hypnose Elmanienne ou Ericksonienne ?</h1>

    <p id="info">
      L’hypnose Elmanienne, développée par Dave Elman, est une méthode
      <strong>rapide et structurée</strong> permettant d’atteindre un état
      hypnotique profond en quelques minutes grâce à des inductions rapides et
      <strong>des suggestions directes</strong>.
    </p>

    <p>
      <strong>
        Elle est souvent utilisée en hypnose thérapeutique et médicale,
        notamment pour la gestion de la douleur, les phobies ou les addictions.
      </strong>
    </p>

    <p>
      En opposition, l’hypnose Ericksonienne, créée par Milton Erickson, repose
      sur une approche plus <strong>subtile et indirecte</strong>. Elle utilise
      des métaphores, des suggestions ouvertes et des histoires pour guider
      l’inconscient vers le changement de manière plus douce et progressive,
      sans confrontation directe.
    </p>

    <p>
      L’hypnose Elmanienne est donc idéale pour des transformations
      <strong>rapides et efficaces</strong>, tandis que l’hypnose Ericksonienne
      convient mieux aux personnes résistantes à l’hypnose ou aux approches
      psychothérapeutiques nécessitant un travail en profondeur.
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
  border: 2px solid rgba(0, 0, 0, 0.3);
  background-color: rgba(255, 255, 255, 0.8);
  border-radius: 15px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  line-height: 1.6;
  text-align: justify;
}

/* Titre principal */
.title {
  color: rgb(135, 89, 210);
  text-align: center;
  font-size: 1.8em;
  margin-bottom: 3vh;
  font-weight: bold;
}

/* Mise en valeur des mots-clés */
strong {
  color: rgb(135, 89, 210);
}

/* Responsive */
@media (max-width: 880px) {
  .definition {
    font-size: 0.9em;
    padding: 4vh 5vw;
  }

  .title {
    font-size: 1.5em;
  }
}
</style>

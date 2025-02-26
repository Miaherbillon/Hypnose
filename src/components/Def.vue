<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="Def">
    <h4 class="Q">L'Hypnose Elmanienne ou Ericksonienne ?</h4>
    <p id="info">
      ... L’hypnose Elmanienne, développée par Dave Elman, est une méthode
      <strong>rapide et structurée</strong> permettant d’atteindre un état
      hypnotique profond en quelques minutes grâce à des inductions rapides et
      <strong>des suggestions directes</strong>.
    </p>

    <p>
      <strong
        >... Elle est souvent utilisée en hypnose thérapeutique et médicale,
        notamment pour la gestion de la douleur, les phobies ou les
        addictions.</strong
      >
    </p>

    <p>
      ... En opposition, l’hypnose Ericksonienne, créée par Milton Erickson,
      repose sur une approche plus <strong>subtile et indirecte</strong>. Elle
      utilise des métaphores, des suggestions ouvertes et des histoires pour
      guider l’inconscient vers le changement de manière plus douce et
      progressive, sans confrontation directe.
    </p>

    <p>
      ... L’hypnose Elmanienne est donc idéale pour des transformations
      <strong>rapides et efficaces</strong>, tandis que l’hypnose Ericksonienne
      convient mieux aux personnes résistantes à l’hypnose ou aux approches
      psychothérapeutiques nécessitant un travail en profondeur.
    </p>
  </div>
</template>

<style scoped>
.Def {
  font-family: "Yuji Syuku", serif;

  width: 70%;
  padding: 2vh 4vw;
  margin: 4vh auto;
  border: 1vh solid #0000006f;
  background-color: rgba(255, 255, 255, 0.618);
  border-radius: 5vh;
}
.Q {
  color: rgb(135, 89, 210);
  display: flex;
  justify-content: center;
  font-size: 1.5em;
  margin: 4vh 0;
  font-weight: 300;
}
strong {
  color: rgb(135, 89, 210);
}
</style>

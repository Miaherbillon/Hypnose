<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Def from "./components/Def.vue";
</script>

<template>
  <div class="ok">
    <HelloWorld msg="M'Hypnose" />
    <Presentation />
    <RendezVous />
    <Def />
  </div>
</template>

<style scoped>
.ok {
  border: 2vh solid #0000006f;
  border-radius: 10vh;
  padding: 2em;
  background-color: rgba(255, 255, 255, 0.764);
}
</style>

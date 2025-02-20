<script setup>
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import rendezVous from "./components/Rendez-vous.vue";
</script>

<template>
  <div class="ok">
    <HelloWorld msg="Vite + Vue" />
    <Presentation />
    <rendezVous />
  </div>
</template>

<style scoped>
.ok {
  border: 2vh solid #0000006f;
  border-radius: 10vh;
  padding: 2em;
  background-color: rgba(255, 255, 255, 0.882);
}
</style>

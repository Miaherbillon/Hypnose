<script setup>
import { ref, onMounted } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Def from "./components/Def.vue";
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";
import Contactez from "./components/Contactez.vue";

const isLoading = ref(true);

onMounted(() => {
  // Un léger délai pour laisser les polices se charger proprement
  setTimeout(() => {
    isLoading.value = false;
  }, 500);
});
</script>

<template>
  <div class="app-container">
    <div v-if="isLoading" class="loader-container">
      <div class="pulse-loader"></div>
      <p class="loader-text">M'Hypnose</p>
    </div>

    <div v-else class="site-wrapper">
      <Menu />
      <div class="page-content">
        <HelloWorld msg="M'Hypnose" />
        <Presentation />
        <RendezVous />
        <Def />
        <Contactez />
      </div>
      <Footer />
    </div>
  </div>
</template>

<style scoped>
.app-container {
  /* Fond beige très clair/rosé pour le côté chaleureux */
  background-color: #ffffff;
  min-height: 100vh;
  font-family: "Quicksand", sans-serif;
}

/* Loader plus doux (pulsation) */
.pulse-loader {
  width: 50px;
  height: 50px;
  background-color: #9b6bc3;
  border-radius: 50%;
  animation: pulse 1.5s infinite ease-in-out;
}

@keyframes pulse {
  0% {
    transform: scale(0.8);
    opacity: 0.5;
  }
  50% {
    transform: scale(1.2);
    opacity: 0.8;
  }
  100% {
    transform: scale(0.8);
    opacity: 0.5;
  }
}

/* Le contenu principal est dans une carte géante flottante */
.page-content {
  max-width: 1100px;
  margin: 0 auto;
  background: white;
  box-shadow: 0 20px 60px rgb(255, 255, 255); /* Ombre très légère */
  border-radius: 40px; /* Coins très arrondis "cocoon" */
  padding: 20px;
  margin-top: 20px;
  margin-bottom: 40px;
}

@media (max-width: 768px) {
  .page-content {
    margin: 10px;
    border-radius: 20px;
  }
}
</style>

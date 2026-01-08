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
  <div class="app-wrapper">
    <div v-if="isLoading" class="loader-container">
      <div class="spinner"></div>
      <p class="loader-text">M'Hypnose Besançon...</p>
    </div>

    <div v-else class="main-layout">
      <Menu /> <HelloWorld msg="M'Hypnose" />
      <Presentation />
      <RendezVous />
      <Def />
      <Contactez />
      <Footer />
    </div>
  </div>
</template>

<style scoped>
/* LOADER AUX COULEURS DU SITE */
.loader-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #fdfaff; /* Fond doux */
}

.spinner {
  width: 60px;
  height: 60px;
  border: 4px solid rgba(135, 89, 210, 0.1);
  border-top: 4px solid rgb(135, 89, 210); /* Ton violet */
  border-radius: 50%;
  animation: spin 1s cubic-bezier(0.68, -0.55, 0.27, 1.55) infinite;
  margin-bottom: 20px;
}

.loader-text {
  font-family: "Poppins", sans-serif;
  color: rgb(135, 89, 210);
  font-weight: 500;
  letter-spacing: 1px;
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

/* STYLE PRINCIPAL - FINI LES BORDURES NOIRES ÉPAISSES */
.main-layout {
  min-height: 100vh;
  background-color: #ffffff;
  /* On retire la grosse bordure noire pour un design plus "aérien" */
  transition: opacity 0.5s ease;
}

/* Si tu veux garder un cadre très léger et élégant, utilise celui-ci : */
/* .main-layout {
  border: 1px solid rgba(135, 89, 210, 0.1);
  margin: 10px;
  border-radius: 20px;
}
*/

@media (max-width: 768px) {
  .main-layout {
    border: none; /* Pas de bordure sur mobile pour gagner de l'espace */
  }
}
</style>

<script setup>
import { ref, onMounted } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Def from "./components/Def.vue";
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";
import Contactez from "./components/Contactez.vue";

// Gestion du chargement
const isLoading = ref(true);

onMounted(() => {
  // Un délai court pour s'assurer que le design est prêt
  setTimeout(() => {
    isLoading.value = false;
  }, 800);
});
</script>

<template>
  <div class="app-container">
    <div v-if="isLoading" class="loader-overlay">
      <div class="breathing-circle"></div>
      <p class="loader-text">M'Hypnose Besançon</p>
    </div>

    <div v-else class="site-layout">
      <Menu />

      <main class="main-bubble">
        <HelloWorld msg="M'Hypnose" />
        <Presentation />
        <RendezVous />
        <Def />
        <Contactez />
      </main>

      <Footer />
    </div>
  </div>
</template>

<style>
/* STYLE GLOBAL (S'applique à toute la page) */
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&family=Playfair+Display:ital,wght@0,700;1,700&display=swap");

body {
  margin: 0;
  padding: 0;
  /* Fond "Beige de lin" très apaisant */
  background-color: #fefaf6;
  font-family: "Quicksand", sans-serif;
  -webkit-font-smoothing: antialiased;
}
</style>

<style scoped>
/* LOADER ANIMATION */
.loader-overlay {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #fefaf6;
}

.breathing-circle {
  width: 60px;
  height: 60px;
  background-color: rgba(155, 107, 195, 0.15);
  border: 2px solid #9b6bc3;
  border-radius: 50%;
  animation: breathe 2s ease-in-out infinite;
}

@keyframes breathe {
  0%,
  100% {
    transform: scale(0.8);
    opacity: 0.5;
  }
  50% {
    transform: scale(1.2);
    opacity: 1;
  }
}

.loader-text {
  margin-top: 25px;
  color: #9b6bc3;
  font-weight: 600;
  letter-spacing: 3px;
  text-transform: uppercase;
  font-size: 0.9em;
}

/* STRUCTURE DU SITE (LA BULLE) */
.site-layout {
  padding: 20px;
  animation: fadeIn 0.8s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(10px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.main-bubble {
  max-width: 1100px;
  margin: 0 auto 40px auto;
  background-color: #ffffff;
  /* On remplace la bordure noire par une ombre douce et un contour violet très fin */
  border-radius: 50px;
  /*box-shadow: 0 20px 60px rgba(155, 107, 195, 0.08);
  /*border: 1px solid rgba(155, 107, 195, 0.05);
  overflow: hidden; /* Pour que les arrondis s'appliquent au contenu */
  padding-bottom: 40px;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .site-layout {
    padding: 10px;
  }
  .main-bubble {
    border-radius: 30px;
    margin-bottom: 20px;
  }
}
</style>

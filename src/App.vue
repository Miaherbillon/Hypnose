<script setup>
import { ref, onMounted } from "vue";
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Def from "./components/Def.vue";
import Menu from "./components/Menu.vue";
// import Contact from "./components/Contact.vue";
import Footer from "./components/Footer.vue";
import Contactez from "./components/Contactez.vue";

// Variable pour gérer l'état du chargement
const isLoading = ref(true);

// Simule un chargement avant d'afficher la page (3s) ////
onMounted(() => {
  setTimeout(() => {
    isLoading.value = false;
  });
});
</script>

<template>
  <div>
    <!-- Écran de chargement -->
    <div v-if="isLoading" class="loader-container">
      <div class="spinner"></div>
      <p>Chargement...</p>
    </div>

    <!-- Contenu principal -->
    <div v-else class="ok">
      <HelloWorld msg="M'Hypnose" />
      <Menu />
      <Presentation />
      <RendezVous />
      <Def />
      <Contactez />
      <Footer />
    </div>
  </div>
</template>

<style scoped>
/* Style pour le chargement */
.loader-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f4f4f4;
  font-size: 1.5em;
  font-weight: bold;
}

/* Animation du spinner */
.spinner {
  width: 50px;
  height: 50px;
  border: 5px solid rgba(0, 0, 0, 0.1);
  border-top: 5px solid #3498db;
  border-radius: 50%;
  animation: spin 1s linear infinite;
  margin-bottom: 10px;
}

@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

/* Style principal */
.ok {
  border: 2vh solid #0000006f;
  border-radius: 10vh;
  padding: 2em;
  background-color: rgba(255, 255, 255, 0.825);
}
</style>

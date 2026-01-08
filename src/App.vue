<script setup>
import { ref, onMounted } from "vue";
// Importation des composants
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Def from "./components/Def.vue";
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";
import Contactez from "./components/Contactez.vue";

const isLoading = ref(true);

onMounted(() => {
  // Délai optimisé pour le ressenti utilisateur
  setTimeout(() => {
    isLoading.value = false;
  }, 600);
});
</script>

<template>
  <div class="app-container">
    <transition name="fade">
      <div
        v-if="isLoading"
        class="loader-container"
        role="alert"
        aria-busy="true">
        <div class="pulse-loader"></div>
        <h1 class="loader-text">M'Hypnose</h1>
      </div>

      <div v-else class="site-wrapper">
        <header>
          <Menu />
        </header>

        <main id="main-content" class="page-content">
          <h1 class="visually-hidden">
            M'Hypnose : Cabinet d'Hypnose, EMDR et PNL
          </h1>

          <HelloWorld msg="M'Hypnose" />

          <section id="presentation">
            <Presentation />
          </section>

          <section id="services">
            <Def />
          </section>

          <section id="rdv">
            <RendezVous />
          </section>

          <section id="contact">
            <Contactez />
          </section>
        </main>

        <Footer />
      </div>
    </transition>
  </div>
</template>

<style scoped>
/* Reset & Base */
.app-container {
  background-color: #fcfafc; /* Un blanc cassé légèrement rosé/violet pour la détente */
  min-height: 100vh;
  font-family: "Quicksand", sans-serif;
  color: #333;
  padding: 20px;
}

/* Loader Styles */
.loader-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.pulse-loader {
  width: 60px;
  height: 60px;
  background-color: #9b6bc3;
  border-radius: 50%;
  box-shadow: 0 0 20px rgba(155, 107, 195, 0.4);
  animation: pulse 1.8s infinite ease-in-out;
}

.loader-text {
  margin-top: 20px;
  font-weight: 300;
  letter-spacing: 3px;
  color: #9b6bc3;
  text-transform: uppercase;
}

/* Animations de transition */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* Conteneur de Page "Cocoon" */
.page-content {
  max-width: 1150px;
  margin: 30px auto;
  background: #ffffff;
  /* Ombre plus douce et diffuse (effet Glassmorphism léger) */
  box-shadow: 0 15px 35px rgba(155, 107, 195, 0.08);
  border-radius: 40px;
  padding: 40px;
  transition: all 0.3s ease;
}

/* Accessibilité SEO : Cache le titre H1 mais le laisse lisible par Google */
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  border: 0;
}

@keyframes pulse {
  0%,
  100% {
    transform: scale(0.8);
    opacity: 0.4;
  }
  50% {
    transform: scale(1.1);
    opacity: 0.7;
  }
}

/* Responsive */
@media (max-width: 768px) {
  .page-content {
    margin: 15px;
    padding: 20px;
    border-radius: 25px;
  }
}
</style>

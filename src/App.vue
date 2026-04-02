<script setup>
import { ref, onMounted } from "vue";

// Importation de tes composants
import HelloWorld from "./components/HelloWorld.vue";
import Presentation from "./components/Presentation.vue";
import Def from "./components/Def.vue";
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";
import RendezVous from "./components/Rendez-vous.vue";
import Contactez from "./components/Contactez.vue";


const isLoading = ref(true);

onMounted(() => {
  setTimeout(() => {
    isLoading.value = false;
  }, 600);
});
</script>

<template>
  <div class="app-container">
    <transition name="fade">
      <div v-if="isLoading" class="loader-overlay">
        <div class="pulse-loader"></div>
        <h1 class="loader-text">M'Hypnose</h1>
      </div>
    </transition>

    <div class="site-layout" :class="{ 'blur-content': isLoading }">
      <main id="main-content">
        <Menu />
        <HelloWorld />

        <Presentation />

        <Def />
        <RendezVous />
        <Contactez />
        <Footer />
      </main>
    </div>
  </div>
</template>

<style>
/* =========================================
   STYLE GLOBAL & FOND DE PAGE (Sans "scoped")
========================================= */
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&family=Playfair+Display:wght@700&display=swap");

body {
  margin: 0;
  padding: 0;
  /* L'image de fond */
  background:
    linear-gradient(rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0.1)),
    url("/007.png");
  background-attachment: fixed;
  background-size: cover;
  background-position: center;
  min-height: 100vh;
  font-family: "Quicksand", sans-serif;
  color: #5a5656;
}

/* =========================================
   LA BULLE PRINCIPALE (EFFET VERRE)
========================================= */
.site-layout {
  width: 92%;
  max-width: 1000px;
  background-color: rgba(255, 255, 255, 0.82);
  backdrop-filter: blur(15px) saturate(140%);
  -webkit-backdrop-filter: blur(15px) saturate(140%);
  border: 1px solid rgba(255, 255, 255, 0.6);
  border-radius: 45px;
  margin: 3vh auto;
  padding: 50px 40px;
  box-shadow: 0 20px 50px rgba(135, 89, 210, 0.1);
  box-sizing: border-box;
  animation: slideUp 1s cubic-bezier(0.16, 1, 0.3, 1);
}

/* Loader Styles */
.loader-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #fcfafc;
  z-index: 9999;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.pulse-loader {
  width: 60px;
  height: 60px;
  background-color: #9b6bc3;
  border-radius: 50%;
  animation: pulse 1.8s infinite ease-in-out;
}
.loader-text {
  margin-top: 20px;
  font-weight: 300;
  letter-spacing: 3px;
  color: #9d80cb;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.blur-content {
  filter: blur(5px);
  overflow: hidden;
  height: 100vh;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
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

/* RESPONSIVE MOBILE */
@media (max-width: 768px) {
  .site-layout {
    width: 95%;
    margin: 15px auto;
    padding: 25px 15px;
    border-radius: 30px;
    backdrop-filter: blur(10px);
  }
}
</style>

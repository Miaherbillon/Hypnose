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
  // 1. GESTION DU LOADER
  setTimeout(() => {
    isLoading.value = false;
  }, 600);

  // 2. SEO - AJOUT EN LIGNE (Sans installation requise)
  // Définition du Titre de l'onglet
  document.title =
    "M'Hypnose - Hypnothérapeute à votre domicile sur Besançon ou en Visio - HERBILLON Mia";

  // Ajout dynamique de la Meta Description pour Google
  let metaDesc = document.querySelector('meta[name="description"]');
  if (!metaDesc) {
    metaDesc = document.createElement("meta");
    metaDesc.name = "description";
    document.head.appendChild(metaDesc);
  }
  metaDesc.content =
    "Cabinet M'Hypnose à votre domicile sur Besançon ou en Visio. Séances d'hypnothérapie pour l'arrêt du tabac, la gestion du stress, la perte de poids et le bien-être.";
});
</script>

<template>
  <div class="app-container">
    <component :is="'script'" type="application/ld+json">
      { "@context": "https://schema.org", "@type": "MedicalBusiness", "name":
      "M'Hypnose", "description": "Cabinet d'hypnothérapie à Besançon.",
      "address": { "@type": "PostalAddress", "streetAddress": "VOTRE ADRESSE
      ICI", "addressLocality": "Besançon", "postalCode": "25000",
      "addressCountry": "FR" }, "priceRange": "$$" }
    </component>

    <transition name="fade">
      <div
        v-if="isLoading"
        class="loader-overlay"
        role="alert"
        aria-busy="true">
        <div class="pulse-loader"></div>
        <h1 class="loader-text">M'Hypnose</h1>
      </div>
    </transition>

    <div class="site-wrapper" :class="{ 'blur-content': isLoading }">
      <header>
        <Menu />
      </header>

      <main id="main-content" class="page-content">
        <h1 class="visually-hidden">
          M'Hypnose - Cabinet d'Hypnose à Besançon
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
  </div>
</template>

<style scoped>
/* Reset & Base */
.app-container {
  min-height: 100vh;
  font-family: "Quicksand", sans-serif;
  color: #333;
  /* On enlève le padding ici pour que le menu puisse toucher les bords si besoin */
  padding: 0;
  position: relative;
  /* background-color: #fcfafc; Fond léger pour tout le site */
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
  box-shadow: 0 0 20px rgba(155, 107, 195, 0.4);
  animation: pulse 1.8s infinite ease-in-out;
}

.loader-text {
  margin-top: 20px;
  font-weight: 300;
  letter-spacing: 3px;
  color: #9d80cb;
  text-transform: uppercase;
}

/* Conteneur de Page - C'est lui qui posait problème */
.page-content {
  max-width: 1150px;
  margin: 30px auto;
  background: rgba(255, 255, 255, 0.6);
  box-shadow: 0 15px 35px rgba(155, 107, 195, 0.08);
  border-radius: 40px;
  padding: 40px;
  transition: all 0.3s ease;
}

/* RESPONSIVE : Le secret est ici */
@media (max-width: 768px) {
  .app-container {
    padding: 0; /* Pas de marge globale */
  }

  .page-content {
    /* Sur mobile, on réduit les marges externes et internes au minimum */
    margin: 10px;
    padding: 15px;
    border-radius: 25px;
    background: transparent; /* On enlève le fond blanc sur mobile pour plus de légèreté */
    box-shadow: none; /* On enlève l'ombre qui peut alourdir le rendu */
  }
}

/* Animations & SEO Utils */
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
</style>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const fullText =
  "M'Hypnose : Votre séance d'hypnose OMNI & Elmanienne en Visio.";
const typedText = ref("");
let index = 0;
let interval = null;

onMounted(() => {
  setTimeout(() => {
    interval = setInterval(() => {
      typedText.value = fullText.slice(0, index);
      index++;
      if (index > fullText.length) {
        clearInterval(interval);
      }
    }, 50);
  }, 500);
});

onUnmounted(() => {
  if (interval) clearInterval(interval);
});
</script>

<template>
  <main class="container">
    <h1 class="visually-hidden">
      M'Hypnose - Mia Herbillon, Praticienne certifiée OMNI Hypnosis
    </h1>

    <header class="hero-section">
      <div class="typed-container" aria-live="polite">
        <p class="typed-heading">
          {{ typedText }}<span class="cursor">|</span>
        </p>
      </div>

      <div class="hero-card">
        <h2 class="section-title">Votre praticienne <strong>OMNI</strong></h2>
        <p class="hero-description">
          Je suis <strong>Mia</strong>, aide-soignante de métier et praticienne
          certifiée
          <a
            href="https://www.mhp-hypnose.com/lhistoire-de-omni"
            target="_blank"
            class="external-link">
            <strong>OMNI Hypnosis *</strong> </a
          >. J'allie mon expertise du soin à la seule méthode d'hypnose au monde
          certifiée
          <a
            href="https://www.mhp-hypnose.com/reconnaissances"
            target="_blank"
            class="external-link">
            <strong>ISO 9001 *</strong> </a
          >. Une approche <strong>orientée résultat</strong> pour transformer
          vos blocages en ressources durables.
        </p>
      </div>
    </header>

    <section class="section-benefits">
      <h2 class="section-title">Pourquoi consulter ?</h2>
      <div class="services-grid">
        <div class="service-card">
          <span class="icon-wrapper">🎯</span>
          <h3>Efficacité</h3>
          <p>Résultats souvent visibles en <strong>1 à 3 séances</strong>.</p>
        </div>
        <div class="service-card">
          <span class="icon-wrapper">💪</span>
          <h3>Confiance</h3>
          <p>Libération émotionnelle et estime de soi.</p>
        </div>
        <div class="service-card">
          <span class="icon-wrapper">⚓</span>
          <h3>Stabilité</h3>
          <p>Gestion du <strong>stress</strong> et des phobies.</p>
        </div>
        <div class="service-card">
          <span class="icon-wrapper">🚬</span>
          <h3>Addictions</h3>
          <p>Protocole OMNI pour le sevrage tabagique.</p>
        </div>
      </div>
    </section>

    <section class="info-card elmanienne">
      <div class="info-content">
        <h2 class="section-title">La Méthode OMNI</h2>
        <p>
          Basée sur les travaux de <strong>Dave Elman</strong>, elle permet
          d'atteindre un état hypnotique profond en quelques minutes pour agir
          directement sur la cause.
        </p>
      </div>
    </section>

    <section class="section-sessions">
      <div class="tarif-card">
        <div class="price-container">
          <span class="price">70</span><span class="currency">€</span>
        </div>
        <p class="duration"><strong>Séance d'environ 1h</strong></p>
        <p class="session-details">En visio</p>
        <a href="#votre-lien-de-rdv" class="button-primary">Prendre RDV</a>
      </div>
    </section>
  </main>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&family=Playfair+Display:wght@700&display=swap");

/* --- BASES --- */
.container {
  font-family: "Quicksand", sans-serif;
  color: #6c6767;
  max-width: 1000px;
  margin: auto;
  line-height: 1.6;
  padding: 20px;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}

strong {
  color: #9d80cb;
  font-weight: 700;
}

/* --- TITRES HARMONISÉS --- */
/* Le titre tout en haut (si tu as un composant Title séparé) doit être plus gros. 
   Ici, nous gérons tous les titres de sections internes. */
.section-title {
  font-family: "Playfair Display", serif;
  font-size: 1.8em; /* Taille fixe pour tous les H2 */
  color: #444;
  text-align: center;
  margin-bottom: 20px;
  line-height: 1.2;
}

/* --- MACHINE À ÉCRIRE --- */
.typed-container {
  min-height: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-bottom: 5px;
}
.typed-heading {
  font-size: 1.2em;
  font-weight: 500;
  color: #888;
}
.cursor {
  color: #9d80cb;
  animation: blink 1s infinite;
}
@keyframes blink {
  50% {
    opacity: 0;
  }
}

/* --- CARTES ET GRILLES --- */
.hero-card,
.tarif-card,
.info-card {
  background: #ffffffa5;
  border-radius: 40px;
  box-shadow: 0 15px 35px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
  text-align: center;
  padding: 35px 25px;
  margin-bottom: 30px;
}

.hero-description {
  font-size: 1.1em;
  color: #666;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin: 25px 0;
}
.service-card {
  background: white;
  padding: 20px 15px;
  border-radius: 25px;
  text-align: center;
  border: 1px solid #f8f8f8;
}
.service-card h3 {
  font-weight: 700;
  font-size: 1.1em;
  color: #9d80cb;
}

/* --- TARIFS --- */
.tarif-card {
  max-width: 350px;
  margin: 30px auto;
}
.price {
  font-size: 4em;
  font-weight: 700;
  color: #9d80cb;
}
.currency {
  font-size: 1.5em;
  vertical-align: super;
  color: #9d80cb;
}

.button-primary {
  display: block;
  background: #9d80cb;
  color: white;
  padding: 15px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 700;
  margin-top: 20px;
  transition: 0.3s;
}

.external-link {
  color: inherit; /* Le lien prend la couleur du texte par défaut */
  text-decoration: none; /* Pas de soulignement */
  transition: all 0.3s ease;
  display: inline-block;
}

.external-link:hover {
  color: #9d80cb; /* Change vers ton mauve au survol */
  transform: translateY(-1px); /* Petit saut vers le haut très léger */
  cursor: pointer;
}

/* Optionnel : un petit changement de gras ou d'opacité si tu préfères */
.external-link:hover strong {
  color: #a63590;
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .container {
    padding: 12px;
  }

  /* On réduit uniformément la taille des titres sur mobile */
  .section-title {
    font-size: 1.2em !important;
    margin-bottom: 15px;
  }

  .typed-container {
    min-height: 40px !important;
  }
  .typed-heading {
    font-size: 0.8em !important;
  }

  .hero-card {
    padding: 25px 15px !important;
  }
  .hero-description {
    font-size: 0.8em !important;
  }

  .services-grid {
    grid-template-columns: repeat(2, 1fr) !important;
  }
  .service-card p {
    font-size: 0.8em !important;
  }

  .price {
    font-size: 3.2em !important;
  }
  .section-title {
    font-size: 1.2em;
  }
  .info-card p {
    font-size: 0.8em;
  }
}
</style>

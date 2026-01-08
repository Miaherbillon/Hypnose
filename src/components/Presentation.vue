<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const typedText = ref("");
const fullText = "M'Hypnose : Votre séance d'hypnose à Besançon et en ligne.";
let index = 0;
let interval = null;

onMounted(() => {
  interval = setInterval(() => {
    typedText.value = fullText.slice(0, index);
    index++;
    if (index > fullText.length) clearInterval(interval);
  }, 70);
});

onUnmounted(() => {
  if (interval) clearInterval(interval);
});
</script>

<template>
  <section class="presentation">
    <h1 class="visually-hidden">Mia Herbillon - Hypnothérapeute à Besançon</h1>

    <header class="header">
      <p aria-hidden="true" class="typed-heading">{{ typedText }}</p>

      <h2 class="main-title">
        Retrouvez votre <span>équilibre</span> intérieur
      </h2>
      <p class="subtitle">Séances d'hypnose Elmanienne à Besançon & en ligne</p>
    </header>

    <div class="cards-grid">
      <div class="card">
        <div class="card-icon">🌿</div>
        <h3>Apaisement</h3>
        <p>
          Libérez-vous du <strong>stress</strong> et de l'anxiété quotidienne.
        </p>
      </div>
      <div class="card active">
        <div class="card-icon">✨</div>
        <h3>Libération</h3>
        <p>Dépassez vos blocages et addictions (tabac, sucre).</p>
      </div>
      <div class="card">
        <div class="card-icon">🌙</div>
        <h3>Sommeil</h3>
        <p>Retrouvez des nuits paisibles et un esprit reposé.</p>
      </div>
    </div>

    <div class="bio-section">
      <div class="bio-text">
        <p>
          Nos émotions peuvent parfois nous submerger. L'<strong
            >hypnose</strong
          >
          offre une approche <strong>douce</strong> pour les explorer et les
          apaiser, vous aidant à surmonter les défis du quotidien à
          <strong>Besançon</strong>.
        </p>
        <div class="cta-wrapper">
          <a href="#rdv" class="btn-warm">Prendre soin de moi</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* Import des polices pour le style moderne */
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&family=Playfair+Display:ital,wght@0,700;1,700&display=swap");

.presentation {
  padding: 60px 20px;
  max-width: 1000px;
  margin: 0 auto;
  font-family: "Quicksand", sans-serif;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
}

.header {
  text-align: center;
  margin-bottom: 50px;
}

/* Style de ton animation de texte */
.typed-heading {
  font-size: 1.3em;
  font-weight: 600;
  color: #9b6bc3;
  min-height: 1.5em;
  margin-bottom: 20px;
  letter-spacing: 0.5px;
}

/* Titre élégant */
.main-title {
  font-family: "Playfair Display", serif;
  font-size: 3em;
  color: #2c2c2c;
  margin-bottom: 10px;
  line-height: 1.2;
}

.main-title span {
  color: #9b6bc3;
  font-style: italic;
}

.subtitle {
  font-size: 1em;
  color: #888;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 40px;
}

/* Grille de cartes */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.card {
  background: #fff;
  padding: 45px 30px;
  border-radius: 35px; /* Coins très arrondis pour le côté cocooning */
  border: 1px solid #f2f2f2;
  transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  text-align: center;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.02);
}

.card:hover {
  transform: translateY(-12px);
  box-shadow: 0 20px 40px rgba(155, 107, 195, 0.12);
  border-color: #e6d5f5;
}

.card.active {
  background: #fdfaff;
  border-color: #e6d5f5;
}

.card-icon {
  font-size: 3em;
  margin-bottom: 20px;
  display: block;
}

.card h3 {
  font-family: "Playfair Display", serif;
  font-size: 1.6em;
  margin-bottom: 15px;
  color: #1a1a1a;
}

/* Section Bio & Bouton */
.bio-section {
  text-align: center;
  max-width: 750px;
  margin: 0 auto;
}

.bio-text p {
  font-size: 1.2em;
  line-height: 1.8;
  color: #555;
  margin-bottom: 35px;
}

.btn-warm {
  display: inline-block;
  background-color: #9b6bc3;
  color: white;
  padding: 20px 45px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1em;
  box-shadow: 0 10px 25px rgba(155, 107, 195, 0.3);
  transition: all 0.3s ease;
}

.btn-warm:hover {
  background-color: #8354ab;
  transform: scale(1.05);
  box-shadow: 0 15px 30px rgba(155, 107, 195, 0.4);
}

/* Adaptations Mobile */
@media (max-width: 768px) {
  .main-title {
    font-size: 2.2em;
  }
  .typed-heading {
    font-size: 1.1em;
  }
  .presentation {
    padding: 40px 15px;
  }
  .card {
    padding: 35px 20px;
  }
}
</style>

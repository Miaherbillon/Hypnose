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
    <header class="header">
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
          Nos émotions peuvent parfois nous submerger. L'hypnose offre une
          approche
          <strong>douce</strong> pour les explorer et les apaiser.
        </p>
        <div class="cta-wrapper">
          <a href="#rdv" class="btn-warm">Prendre soin de moi</a>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.presentation {
  padding: 40px 20px;
}

/* Titre élégant (Playfair Display) */
.main-title {
  font-family: "Playfair Display", serif;
  font-size: 2.8em;
  color: #2c2c2c;
  margin-bottom: 10px;
}

.main-title span {
  color: #9b6bc3;
  font-style: italic;
}

.subtitle {
  font-size: 1.1em;
  color: #777;
  letter-spacing: 1px;
  margin-bottom: 50px;
}

/* Grille de cartes "Style" */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  margin-bottom: 60px;
}

.card {
  background: #fff;
  padding: 40px 30px;
  border-radius: 30px;
  border: 1px solid #f0f0f0;
  transition: all 0.4s ease;
  text-align: center;
}

.card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(155, 107, 195, 0.1);
  border-color: #9b6bc3;
}

/* Carte mise en avant */
.card.active {
  background: #fdf8ff;
  border-color: #e6d5f5;
}

.card-icon {
  font-size: 2.5em;
  margin-bottom: 20px;
  display: block;
}

/* Bouton Chaleureux */
.btn-warm {
  display: inline-block;
  background-color: #9b6bc3;
  color: white;
  padding: 18px 40px;
  border-radius: 50px; /* Bouton "pilule" très moderne */
  text-decoration: none;
  font-weight: 600;
  box-shadow: 0 10px 20px rgba(155, 107, 195, 0.2);
  transition: all 0.3s ease;
}

.btn-warm:hover {
  background-color: #8354ab;
  transform: scale(1.05);
}

@media (max-width: 768px) {
  .main-title {
    font-size: 2em;
  }
}
</style>

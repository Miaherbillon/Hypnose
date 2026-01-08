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
  <main class="container">
    <h1 class="visually-hidden">
      M'Hypnose - Mia Herbillon, Hypnothérapeute à Besançon et séances en ligne
    </h1>

    <header class="hero-section">
      <p aria-hidden="true" class="typed-heading">{{ typedText }}</p>
      <div class="hero-card">
        <h2>
          Votre praticienne en <strong>hypnose</strong> à
          <strong>Besançon (25000)</strong>
        </h2>
        <p>
          Je suis Mia, praticienne certifiée en
          <strong>hypnose Elmanienne</strong>. Je vous accompagne avec
          bienveillance dans mon cabinet ou à distance pour un
          <strong>bien-être</strong> durable.
        </p>
      </div>
    </header>

    <section class="section-benefits">
      <h2 class="section-title">Pourquoi consulter à Besançon ?</h2>
      <div class="services-grid">
        <div class="service-card">
          <div class="icon">✨</div>
          <h3>Libération</h3>
          <p>Anxiété, <strong>stress</strong> et phobies.</p>
        </div>
        <div class="service-card">
          <div class="icon">💪</div>
          <h3>Confiance</h3>
          <p>Estime de soi et blocages émotionnels.</p>
        </div>
        <div class="service-card">
          <div class="icon">😴</div>
          <h3>Sommeil</h3>
          <p>Retrouvez des nuits calmes et réparatrices.</p>
        </div>
        <div class="service-card">
          <div class="icon">🚬</div>
          <h3>Addictions</h3>
          <p>Aide au <strong>sevrage tabagique</strong> efficace.</p>
        </div>
      </div>
    </section>

    <section class="info-card elmanienne">
      <h2>L'Hypnose Elmanienne</h2>
      <p>
        Une méthode <strong>rapide et directe</strong>, reconnue pour son
        efficacité à résoudre des problématiques spécifiques. Idéal pour ceux
        qui cherchent des résultats concrets à <strong>Besançon</strong>.
      </p>
      <a href="#info" class="link-more-info">Découvrir la méthode Omni →</a>
    </section>

    <section class="section-sessions">
      <div class="tarif-card">
        <div class="badge">Séance Individuelle</div>
        <div class="price">70€</div>
        <p>Durée : 1 heure environ</p>
        <p>À distance via Google Meet ou en cabinet.</p>
        <a href="#votre-lien-de-rdv" class="button-primary"
          >Réserver mon créneau</a
        >
      </div>
    </section>

    <footer class="section-cta">
      <h2>Prêt(e) pour le changement ?</h2>
      <p>Contactez-moi pour planifier votre séance d'hypnose personnalisée.</p>
    </footer>
  </main>
</template>

<style scoped>
/* BASES ET TYPOGRAPHIE */
.container {
  font-family: "Poppins", sans-serif;
  color: #2d2d2d;
  width: 90%;
  max-width: 900px;
  margin: auto;
  line-height: 1.6;
  padding: 40px 0;
}

.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
}

strong {
  color: rgb(135, 89, 210);
  font-weight: 600;
}

/* HERO SECTION */
.hero-section {
  text-align: center;
  margin-bottom: 60px;
}

.typed-heading {
  font-size: 1.6em;
  font-weight: bold;
  color: #1a1a1a;
  min-height: 2em;
  margin-bottom: 20px;
}

.hero-card {
  background-color: #fdfaff;
  padding: 40px;
  border-radius: 24px;
  box-shadow: 0 10px 30px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
}

/* SERVICES GRID */
.section-title {
  text-align: center;
  margin-bottom: 40px;
  font-size: 1.8em;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
  margin-bottom: 60px;
}

.service-card {
  background: white;
  padding: 30px 20px;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 30px rgba(135, 89, 210, 0.12);
}

.service-card .icon {
  font-size: 2.5em;
  margin-bottom: 15px;
}

.service-card h3 {
  margin-bottom: 10px;
  color: #1a1a1a;
}

/* INFO CARD (ELMANIENNE) */
.info-card {
  background: #f8f9fa;
  padding: 40px;
  border-radius: 24px;
  margin-bottom: 60px;
  text-align: center;
}

/* TARIF CARD */
.tarif-card {
  background: white;
  border: 2px solid #f0eaff;
  padding: 50px 20px;
  border-radius: 30px;
  text-align: center;
  max-width: 400px;
  margin: 0 auto 60px;
  box-shadow: 0 15px 40px rgba(135, 89, 210, 0.08);
}

.price {
  font-size: 3.5em;
  font-weight: bold;
  color: rgb(135, 89, 210);
  margin: 15px 0;
}

.badge {
  display: inline-block;
  background: #f0eaff;
  color: rgb(135, 89, 210);
  padding: 5px 15px;
  border-radius: 20px;
  font-size: 0.9em;
  font-weight: bold;
}

/* BOUTON */
.button-primary {
  display: inline-block;
  background-color: rgb(135, 89, 210);
  color: white;
  padding: 18px 35px;
  border-radius: 12px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 25px;
  transition: background 0.3s, transform 0.2s;
}

.button-primary:hover {
  background-color: rgb(110, 60, 180);
  transform: scale(1.05);
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .hero-card {
    padding: 25px;
  }
  .price {
    font-size: 2.5em;
  }
  .typed-heading {
    font-size: 1.2em;
  }
}
</style>

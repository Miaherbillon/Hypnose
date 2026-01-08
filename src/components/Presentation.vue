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
          <strong>Besançon (25000)</strong> et <strong>en ligne</strong>
        </h2>
        <p>
          Je suis Mia, praticienne certifiée en
          <strong>hypnose Elmanienne</strong>. Formée par l'école suisse Omni
          depuis 2020, je vous accompagne avec bienveillance dans mon cabinet de
          <strong>Besançon</strong> ou à distance vers un
          <strong>bien-être</strong> durable.
        </p>
        <p class="sub-text">
          Que vous habitiez à <strong>Besançon</strong>, dans le Doubs, ou
          partout ailleurs en France, mes séances s'adaptent à vos besoins grâce
          à la flexibilité de l'offre en ligne.
        </p>
      </div>
    </header>

    <section class="section-benefits">
      <h2 class="section-title">
        Pourquoi consulter pour de l'<strong>hypnose à Besançon</strong> ?
      </h2>

      <div class="intro-benefits">
        <p>
          Nos émotions peuvent parfois nous submerger. L'hypnose offre une
          approche douce pour les explorer et les apaiser.
        </p>
      </div>

      <div class="services-grid">
        <div class="service-card">
          <div class="icon">✅</div>
          <h3>Libération</h3>
          <p>
            Gestion de l'anxiété, du <strong>stress</strong> et des phobies à
            Besançon.
          </p>
        </div>
        <div class="service-card">
          <div class="icon">💪</div>
          <h3>Confiance</h3>
          <p>Renforcement de l'estime de soi et dépassement des blocages.</p>
        </div>
        <div class="service-card">
          <div class="icon">😴</div>
          <h3>Sommeil</h3>
          <p>Amélioration de la qualité de vos nuits et relaxation profonde.</p>
        </div>
        <div class="service-card">
          <div class="icon">🚬</div>
          <h3>Addictions</h3>
          <p>
            Gestion des addictions et <strong>sevrage tabagique</strong> par
            l'hypnose.
          </p>
        </div>
        <div class="service-card">
          <div class="icon">🤕</div>
          <h3>Douleurs</h3>
          <p>Atténuation des douleurs chroniques (en complément médical).</p>
        </div>
      </div>
    </section>

    <section class="info-card elmanienne">
      <h2>L'Hypnose Elmanienne</h2>
      <p>
        Une méthode <strong>rapide et directe</strong>, reconnue pour son
        efficacité à résoudre des problématiques spécifiques. Cette technique
        favorise un état de transe profonde permettant des résultats concrets à
        <strong>Besançon</strong>.
      </p>
      <a href="#info" class="link-more-info">Découvrir la méthode Omni →</a>
    </section>

    <section class="section-sessions">
      <div class="tarif-card">
        <div class="badge">Séance Individuelle</div>
        <div class="price">70€</div>
        <p><strong>Durée : 1 heure environ</strong></p>
        <p>
          Séances réalisées sereinement à distance (Google Meet) ou en cabinet à
          Besançon.
        </p>
        <a href="#votre-lien-de-rdv" class="button-primary"
          >Réserver mon créneau</a
        >
      </div>
    </section>

    <footer class="section-cta">
      <h2>Prêt(e) pour le changement ?</h2>
      <p>
        Contactez-moi dès aujourd'hui pour planifier votre
        <strong>séance d'hypnose à Besançon</strong> ou en visio.
      </p>
    </footer>
  </main>
</template>

<style scoped>
/* BASES ET TYPOGRAPHIE 2026 */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Playfair+Display:wght@700&display=swap");

.container {
  font-family: "Poppins", sans-serif;
  color: #2d2d2d;
  width: 90%;
  max-width: 950px;
  margin: auto;
  line-height: 1.7;
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
  border-radius: 30px;
  box-shadow: 0 10px 30px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
}

.sub-text {
  font-size: 0.95em;
  color: #666;
  margin-top: 15px;
}

/* SERVICES GRID */
.section-title {
  font-family: "Playfair Display", serif;
  text-align: center;
  margin-bottom: 20px;
  font-size: 2.2em;
}

.intro-benefits {
  text-align: center;
  max-width: 700px;
  margin: 0 auto 40px;
  color: #555;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 25px;
  margin-bottom: 60px;
}

.service-card {
  background: white;
  padding: 35px 25px;
  border-radius: 25px;
  text-align: center;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03);
  transition: all 0.3s ease;
  border: 1px solid #f9f9f9;
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(135, 89, 210, 0.1);
  border-color: rgba(135, 89, 210, 0.2);
}

.service-card .icon {
  font-size: 2.5em;
  margin-bottom: 15px;
}

.service-card h3 {
  font-family: "Playfair Display", serif;
  margin-bottom: 12px;
  font-size: 1.4em;
}

/* INFO CARD */
.info-card {
  background: #f8f9fa;
  padding: 50px 40px;
  border-radius: 30px;
  margin-bottom: 60px;
  text-align: center;
}

.link-more-info {
  display: inline-block;
  margin-top: 20px;
  color: rgb(135, 89, 210);
  text-decoration: none;
  font-weight: 600;
}

/* TARIF CARD */
.tarif-card {
  background: white;
  border: 1px solid #f0eaff;
  padding: 50px 30px;
  border-radius: 40px;
  text-align: center;
  max-width: 450px;
  margin: 0 auto 60px;
  box-shadow: 0 20px 50px rgba(135, 89, 210, 0.08);
}

.price {
  font-size: 4em;
  font-weight: bold;
  color: rgb(135, 89, 210);
  margin: 10px 0;
}

.badge {
  display: inline-block;
  background: #f0eaff;
  color: rgb(135, 89, 210);
  padding: 6px 20px;
  border-radius: 25px;
  font-size: 0.9em;
  font-weight: bold;
}

/* BOUTON */
.button-primary {
  display: inline-block;
  background-color: rgb(135, 89, 210);
  color: white;
  padding: 20px 40px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: bold;
  margin-top: 30px;
  box-shadow: 0 10px 20px rgba(135, 89, 210, 0.2);
  transition: all 0.3s ease;
}

.button-primary:hover {
  background-color: rgb(110, 60, 180);
  transform: scale(1.05);
  box-shadow: 0 15px 30px rgba(135, 89, 210, 0.3);
}

.section-cta {
  text-align: center;
  padding: 40px 0;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .container {
    width: 95%;
  }
  .section-title {
    font-size: 1.8em;
  }
  .hero-card {
    padding: 25px;
  }
  .price {
    font-size: 3em;
  }
  .typed-heading {
    font-size: 1.2em;
  }
}
</style>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const fullText = "M'Hypnose : Votre séance d'hypnose en ligne et à Besançon.";
const typedText = ref("");
let index = 0;
let interval = null;

onMounted(() => {
  // On commence l'animation après un court délai
  setTimeout(() => {
    interval = setInterval(() => {
      typedText.value = fullText.slice(0, index);
      index++;
      if (index > fullText.length) {
        clearInterval(interval);
      }
    }, 60);
  }, 500);
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
      <div class="typed-container" aria-live="polite">
        <p class="typed-heading" aria-hidden="true">
          {{ typedText }}<span class="cursor">|</span>
        </p>
        <p class="visually-hidden">{{ fullText }}</p>
      </div>

      <div class="hero-card">
        <h2 class="hero-title">
          Votre praticienne en <strong>hypnose</strong> à
          <span class="city-tag">Besançon (25000)</span> et
          <strong>en ligne</strong>
        </h2>
        <p class="hero-description">
          Je suis <strong>Mia</strong>, praticienne certifiée en
          <strong>hypnose Elmanienne</strong>. Formée par l'école suisse
          <strong>Omni</strong>, je vous accompagne avec bienveillance à
          domicile secteur de <strong>Besançon</strong> ou à distance vers un
          <strong>bien-être</strong> durable.
        </p>
        <p class="sub-text">
          Que vous habitiez dans le Doubs ou partout ailleurs en France, mes
          séances s'adaptent à vos besoins en visio ou en présentiel.
        </p>
      </div>
    </header>

    <section class="section-benefits">
      <h2 class="section-title">
        Pourquoi consulter pour de l'<strong>hypnose à Besançon</strong> ?
      </h2>

      <div class="services-grid">
        <div class="service-card">
          <div class="icon-wrapper">✅</div>
          <h3>Libération</h3>
          <p>
            Gestion de l'anxiété, du <strong>stress</strong> et des phobies.
          </p>
        </div>
        <div class="service-card">
          <div class="icon-wrapper">💪</div>
          <h3>Confiance</h3>
          <p>Renforcement de l'estime de soi et dépassement des blocages.</p>
        </div>
        <div class="service-card">
          <div class="icon-wrapper">😴</div>
          <h3>Sommeil</h3>
          <p>Retrouvez des nuits paisibles et une relaxation profonde.</p>
        </div>
        <div class="service-card">
          <div class="icon-wrapper">🚬</div>
          <h3>Addictions</h3>
          <p>Sevrage tabagique et gestion des dépendances par l'hypnose.</p>
        </div>
      </div>
    </section>

    <section class="info-card elmanienne">
      <div class="info-content">
        <h2>L'Hypnose Elmanienne</h2>
        <p>
          Une méthode <strong>rapide et directe</strong>, reconnue mondialement
          pour son efficacité. Cette technique favorise un état de transe
          profonde permettant des résultats concrets à
          <strong>Besançon</strong>.
        </p>
        <a href="#info" class="link-more-info">Découvrir la méthode Omni →</a>
      </div>
    </section>

    <section class="section-sessions">
      <div class="tarif-card">
        <div class="badge">Séance Individuelle</div>
        <div class="price-container">
          <span class="price">70</span><span class="currency">€</span>
        </div>
        <p class="duration"><strong>Durée : 1 heure environ</strong></p>
        <p class="session-details">
          Séances réalisées sereinement en ligne (Google Meet) ou à domicile.
        </p>
        <a href="#votre-lien-de-rdv" class="button-primary"
          >Réserver mon créneau</a
        >
      </div>
    </section>
  </main>
</template>

<style scoped>
/* POLICES */
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&family=Playfair+Display:wght@700&display=swap");

.container {
  font-family: "Quicksand", sans-serif;
  color: #333;
  max-width: 1000px;
  margin: auto;
  line-height: 1.8;
  padding: 20px;
}

/* SEO UTILS */
.visually-hidden {
  background: #ffffffa5;
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
  color: #8759d2;
  font-weight: 700;
}

/* HERO */
.typed-container {
  min-height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.typed-heading {
  font-size: 1.8em;
  font-weight: 700;
  color: #2d2d2d;
  margin: 0;
}

.cursor {
  color: #8759d2;
  animation: blink 1s infinite;
}

@keyframes blink {
  50% {
    opacity: 0;
  }
}

.hero-card {
  background: #ffffffa5;
  padding: 50px 30px;
  border-radius: 40px;
  box-shadow: 0 20px 40px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
  margin-top: 20px;
}

.hero-title {
  font-family: "Playfair Display", serif;
  font-size: 2.2em;
  margin-bottom: 20px;
  line-height: 1.3;
}

.city-tag {
  background: #ffffffa5;
  padding: 2px 10px;
  border-radius: 8px;
  color: #8759d2;
}

/* SERVICES */
.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 25px;
  margin: 40px 0;
}

.service-card {
  background: #ffffffa5;
  padding: 30px;
  border-radius: 30px;
  text-align: center;
  border: 1px solid #f1f1f1;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.service-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 30px rgba(135, 89, 210, 0.1);
}

.icon-wrapper {
  font-size: 2.5em;
  margin-bottom: 15px;
  display: block;
}

/* TARIF CARD */
.tarif-card {
  background: #ffffffa5;
  padding: 40px;
  border-radius: 40px;
  text-align: center;
  max-width: 400px;
  margin: 40px auto;
  box-shadow: 0 20px 50px rgba(135, 89, 210, 0.12);
  border: 1px solid #f0eaff;
}

.price {
  font-size: 5em;
  font-weight: 700;
  color: #8759d2;
  letter-spacing: -2px;
}

.currency {
  font-size: 2em;
  vertical-align: super;
  color: #8759d2;
}

.button-primary {
  display: block;
  background: #8759d2;
  color: white;
  padding: 18px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 700;
  transition: all 0.3s ease;
  margin-top: 25px;
}

.button-primary:hover {
  background: #6e3cb4;
  box-shadow: 0 10px 20px rgba(110, 60, 180, 0.3);
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .hero-title {
    font-size: 1.6em;
  }
  .price {
    font-size: 4em;
  }
  .typed-heading {
    font-size: 1.3em;
  }
}
</style>

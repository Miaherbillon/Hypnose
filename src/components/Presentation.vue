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
      if (index > fullText.length) clearInterval(interval);
    }, 50);
  }, 500);
});

onUnmounted(() => {
  if (interval) clearInterval(interval);
});
</script>

<template>
  <div class="content-wrapper">
    <div class="typed-container" aria-live="polite">
      <p class="typed-heading">{{ typedText }}<span class="cursor">|</span></p>
    </div>

    <div class="hero-card">
      <div class="card">
        <div>
          <h2 class="section-title">Votre praticienne <strong>OMNI</strong></h2>
          <h2>Herbillon Mia</h2>
        </div>
        <img src="/mia1.png" alt="Photo de Mia" class="Mia" />
      </div>

      <p class="hero-description">
        Forte de mon expérience d'<strong>aide-soignante</strong>, le soin et
        l'écoute sont au cœur de mon accompagnement. Formée au sein du cursus
        <strong>MHP Hypnose</strong>, j'utilise la méthode
        <strong>OMNI</strong>, une approche
        <strong>Elmanienne moderne</strong> qui va droit au but. <br /><br />
        Mon objectif : atteindre rapidement un état hypnotique profond pour
        transformer vos blocages en ressources, avec une approche
        <strong>pragmatique et bienveillante</strong>.
      </p>
    </div>

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

    <div class="info-card">
      <h2 class="section-title">La Méthode OMNI</h2>

      <div class="method-intro">
        <p>
          J'utilise la <strong>méthode OMNI</strong>, une approche
          <strong>Elmanienne</strong> moderne.
        </p>
        <p>
          Là où l'hypnose classique cherche à "masser" le problème par des
          métaphores, la méthode Elmanienne va droit au but : elle utilise une
          induction rapide pour atteindre un état de relaxation profonde (le
          <strong>somnambulisme hypnotique</strong>) en quelques minutes
          seulement.
        </p>
      </div>

      <div class="method-highlights">
        <div class="highlight-item">
          <span class="highlight-icon">🎯</span>
          <p>
            <strong>Direct :</strong> On agit sur la cause racine, pas juste le
            symptôme.
          </p>
        </div>
        <div class="highlight-item">
          <span class="highlight-icon">⚡</span>
          <p>
            <strong>Rapide :</strong> Plus de temps pour le travail
            thérapeutique réel.
          </p>
        </div>
        <div class="highlight-item"></div>
      </div>
    </div>

    <div class="tarif-card">
      <div class="price-container">
        <span class="price">70</span><span class="currency">€</span>
      </div>
      <p><strong>Séance d'environ 1h</strong></p>
      <p>Visio ou domicile (Besançon).</p>
      <a href="#votre-lien-de-rdv" class="button-primary"
        >Réserver une séance</a
      >
    </div>
  </div>
</template>

<style scoped>
strong {
  color: #9d80cb;
  font-weight: 700;
}

/* Liens discrets */
.external-link {
  color: inherit;
  text-decoration: none;
  transition: all 0.3s ease;
  display: inline-block;
}
.external-link:hover {
  color: #9d80cb;
  transform: translateY(-1px);
  cursor: pointer;
}
.external-link:hover strong {
  color: #9d80cb;
}

/* Titres H2 Harmonieux */
.section-title {
  font-family: "Playfair Display", serif;
  font-size: 1.8em;
  color: #000000;
  text-align: center;
  margin-bottom: 20px;
  line-height: 1.2;
}

/* Typage */
.typed-container {
  min-height: 40px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  margin-bottom: 20px;
}
.typed-heading {
  font-size: 1.2em;
  font-weight: 500;
  color: #888;
  margin: 0;
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

/* Cartes (Hero, Info, Tarif) */
.hero-card,
.info-card,
.tarif-card {
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
  line-height: 1.6;
}

/* Grille des services */
.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
  margin-bottom: 40px;
}
.service-card {
  background: white;
  padding: 20px 15px;
  border-radius: 25px;
  text-align: center;
  border: 1px solid #f8f8f8;
}
.icon-wrapper {
  font-size: 2em;
  display: block;
  margin-bottom: 10px;
}
.service-card h3 {
  font-weight: 700;
  font-size: 1.1em;
  color: #9d80cb;
  margin-bottom: 5px;
}

/* Bouton et Prix */
.tarif-card {
  max-width: 350px;
  margin: 0 auto;
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
.button-primary:hover {
  background: #8265b5;
  transform: scale(1.02);
}

.card {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  gap: 20px;
  text-align: right;
  font-size: 1.2em;
}
.Mia {
  width: 13em;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1em 0;
}

/* RESPONSIVE MOBILE */
@media (max-width: 768px) {
  .section-title {
    font-size: 1em;
  }
  .typed-heading {
    font-size: 0.95em;
  }
  .hero-card,
  .info-card,
  .tarif-card {
    padding: 25px 15px;
    border-radius: 30px;
  }
  .hero-description {
    font-size: 0.95em;
  }
  .services-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
  }
  .service-card {
    padding: 15px 10px;
    border-radius: 20px;
  }
  .service-card h3 {
    font-size: 1em;
  }
  .service-card p {
    font-size: 0.85em;
  }
  .price {
    font-size: 3.2em;
  }
  .card {
    display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 0.3em;
    text-align: right;
    font-size: 0.7em;
  }
  .Mia {
    width: 7em;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const typedText = ref("");
// Texte d'accroche optimisé SEO
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

    <p aria-hidden="true" class="typed-heading">{{ typedText }}</p>

    <section class="section-intro">
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
      <p>
        Que vous habitiez à <strong>Besançon</strong>, dans le Doubs, ou partout
        ailleurs en France, mes séances d'<strong>hypnose</strong> s'adaptent à
        vos besoins grâce à la flexibilité de l'accompagnement
        <strong>en ligne</strong>. L'<strong>hypnose</strong>
        est une rencontre profonde avec soi-même pour une transformation
        positive.
      </p>
    </section>

    <hr class="separator" />

    <section class="section-benefits">
      <h2>
        Pourquoi consulter pour de l'<strong>hypnose à Besançon</strong> ?
      </h2>
      <p>
        Nos émotions peuvent parfois nous submerger. L'<strong>hypnose</strong>
        offre une approche douce pour les explorer et les apaiser, vous aidant à
        surmonter les défis du quotidien.
      </p>
      <p>
        Grâce à l'<strong>hypnose</strong>, il est possible de retrouver un
        profond <strong>bien-être</strong> en vous accompagnant pour :
      </p>
      <ul class="seo-list">
        <li>
          ✅ <strong>Libération émotionnelle :</strong> gestion de l'anxiété, du
          <strong>stress</strong> et des phobies à Besançon.
        </li>
        <li>
          💪 <strong>Confiance en soi :</strong> renforcement de l'estime de soi
          et dépassement des blocages.
        </li>
        <li>
          😴 <strong>Sommeil :</strong> amélioration de la qualité de vos nuits
          et relaxation profonde.
        </li>
        <li>
          🚬 <strong>Arrêt du tabac :</strong> gestion des
          <strong>addictions</strong> et sevrage tabagique par l'hypnose.
        </li>
        <li>
          🤕 <strong>Douleurs :</strong> atténuation des douleurs chroniques (en
          complément médical).
        </li>
      </ul>
      <p>
        Que votre objectif soit la gestion du <strong>stress</strong> ou le
        sevrage tabagique, l'<strong>hypnose à Besançon</strong> ou à distance
        est un chemin efficace.
      </p>
    </section>

    <hr class="separator" />

    <section class="section-elmanienne">
      <h2>
        <strong>Hypnose Elmanienne</strong> : Une méthode rapide à Besançon
      </h2>
      <p>
        Cette technique est reconnue pour être directe et efficace. L'<strong
          >hypnose Elmanienne</strong
        >
        favorise un état de transe profonde permettant de résoudre des
        problématiques spécifiques rapidement.
      </p>
      <a href="#info" class="link-more-info"
        >En savoir plus sur l'approche Omni Hypnosis</a
      >
    </section>

    <section class="section-sessions">
      <h2>Séances d'<strong>hypnose en ligne</strong> et tarifs</h2>
      <p>
        Je vous propose des séances d'une heure via Google Meet. Profitez de mon
        expertise en <strong>hypnose</strong> où que vous soyez, que vous soyez
        résident à <strong>Besançon</strong> ou ailleurs.
      </p>

      <div class="tarif-box">
        <p>💰 <strong>Tarif : 70 euros la séance</strong></p>
        <p>
          Réservez votre séance de <strong>bien-être</strong> dès maintenant.
        </p>
        <a href="#votre-lien-de-rdv" class="button-primary"
          >Prendre rendez-vous en ligne</a
        >
      </div>
    </section>

    <section class="section-cta">
      <h2>Prêt(e) à changer avec l'<strong>hypnose</strong> ?</h2>
      <p>
        Contactez-moi pour planifier votre
        <strong>séance d'hypnose à Besançon</strong> ou en visio.
      </p>
    </section>
  </main>
</template>

<style scoped>
/* Ajout pour le SEO : Masque le H1 tout en le laissant lisible par Google */
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

.container {
  font-family: "Yuji Syuku", serif;
  width: 90%;
  max-width: 800px;
  margin: auto;
  line-height: 1.6;
  padding: 20px 0;
}

strong {
  color: rgb(100, 50, 180);
}

.typed-heading {
  font-size: 1.5em;
  font-weight: bold;
  text-align: center;
  color: #000;
  border-right: 2px solid black;
  display: block;
  width: max-content;
  margin: 0 auto 1em auto;
  white-space: nowrap;
  overflow: hidden;
  animation: blinkCursor 0.8s infinite step-end;
}

@keyframes blinkCursor {
  50% {
    border-color: transparent;
  }
}

h2 {
  font-size: 1.6em;
  text-align: center;
  margin-top: 2em;
  margin-bottom: 0.8em;
}

p {
  text-align: justify;
  margin-bottom: 1em;
}

.seo-list {
  list-style: none;
  padding: 0;
}

.seo-list li {
  text-align: left;
  margin-bottom: 0.8em;
  padding-left: 5px;
}

.button-primary {
  display: inline-block;
  background-color: rgb(135, 89, 210);
  color: white;
  padding: 15px 30px;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.2s;
}

.button-primary:hover {
  transform: translateY(-2px);
  background-color: rgba(135, 89, 210, 0.9);
}

.tarif-box {
  border: 1px solid #eee;
  padding: 2em;
  border-radius: 15px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.05);
  text-align: center;
}

@media (max-width: 768px) {
  .typed-heading {
    font-size: 1.1em;
    white-space: normal;
    width: 100%;
    border: none;
  }
  p {
    text-align: left;
  }
}
</style>

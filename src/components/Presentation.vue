<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const typedText = ref("");
// Ajout des mots-clés "Besançon" et "Hypnose Elmanienne" directement dans le texte d'introduction pour le SEO
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
    <h1 aria-live="polite" class="typed-heading">{{ typedText }}</h1>

    <section class="section-intro">
      <h2>
        Votre praticienne en <strong>hypnose</strong> à
        <strong>Besançon</strong> et <strong>en ligne</strong>
      </h2>
      <p>
        Je suis Mia, praticienne certifiée en
        <strong>hypnose Elmanienne</strong>. Formée par l'école suisse Omni
        depuis 2020, je vous accompagne avec bienveillance vers un meilleur
        <strong>bien-être</strong> durable.
      </p>
      <p>
        Que vous soyez à <strong>Besançon</strong>, en Franche-Comté, ou partout
        ailleurs, nos séances d'<strong>hypnose</strong> s'adaptent à vous grâce
        à la flexibilité de l'offre <strong>en ligne</strong>. L'<strong
          >hypnose</strong
        >
        est une rencontre profonde avec soi-même, un espace de transformation
        positive vers la sérénité et le **mieux-être**.
      </p>
    </section>

    <hr class="separator" />

    <section class="section-demystification">
      <h2>
        L'<strong>hypnose</strong> : Reprendre le contrôle de votre esprit
      </h2>
      <p>
        <strong>
          Loin des clichés, l'<strong>hypnose</strong> est un état naturel de
          conscience modifiée. Il ne s'agit pas de perdre le contrôle, mais de
          retrouver vos propres ressources intérieures pour un changement
          positif et durable.
        </strong>
      </p>
    </section>

    <hr class="separator" />

    <section class="section-benefits">
      <h2>
        Les bienfaits de l'<strong>hypnose</strong> pour votre
        <strong>mieux-être</strong>
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
      <ul>
        <li>
          ✅ La libération d'émotions et de blocages (comme l'anxiété, le
          <strong>stress</strong>, les phobies).
        </li>
        <li>💪 Le renforcement de l'estime de soi et de la confiance.</li>
        <li>
          😴 L'amélioration de la qualité de votre <strong>sommeil</strong>.
        </li>
        <li>
          🚬 La gestion des <strong>addictions</strong> (aide au
          <strong>sevrage tabagique</strong>, etc.).
        </li>
        <li>
          🤕 L'atténuation de certaines <strong>douleurs chroniques</strong> (en
          complément d'un suivi médical).
        </li>
      </ul>
      <p>
        Que votre objectif soit la gestion du <strong>stress</strong>, la
        diminution de l'anxiété ou l'amélioration du <strong>sommeil</strong>,
        l'<strong>hypnose</strong> à <strong>Besançon</strong> ou à distance est
        un chemin efficace vers la solution.
      </p>
    </section>

    <hr class="separator" />

    <section class="section-elmanienne">
      <h2>
        <strong>Hypnose Elmanienne</strong> : Une méthode ciblée et efficace
      </h2>
      <p>
        Cette technique est rapide et directe, favorisant un état d'<strong
          >hypnose</strong
        >
        profonde. L'<strong>hypnose Elmanienne</strong> est reconnue pour son
        efficacité dans la résolution de problématiques spécifiques et le
        renforcement de vos ressources personnelles.
      </p>
      <a href="#info" class="link-more-info"
        >En savoir plus sur cette approche d'<strong>hypnose</strong></a
      >
    </section>

    <section class="section-sessions">
      <h2>
        Séances d'<strong>hypnose en ligne</strong> : Confort et flexibilité
      </h2>
      <p>
        Je vous propose des séances d'<strong>hypnose</strong> d'une heure,
        réalisées sereinement à distance via Google Meet. Bénéficiez de mes
        services où que vous soyez, y compris si vous êtes à
        <strong>Besançon</strong> et préférez le confort de votre domicile.
      </p>

      <div class="tarif-box">
        <p>💰 Tarif : 70 euros la séance</p>
        <p>
          Réservez votre moment de <strong>bien-être</strong> dès maintenant.
        </p>
        <a href="#votre-lien-de-rdv" class="button-primary"
          >Prendre rendez-vous <strong>en ligne</strong></a
        >
      </div>
    </section>

    <section class="section-preparation">
      <h2>
        Préparez votre <strong>séance d'hypnose</strong> à distance pour une
        expérience optimale
      </h2>
      <p>Pour une séance réussie, prévoyez :</p>
      <ul>
        <li>✅ Une connexion internet stable.</li>
        <li>🎧 Un casque ou des écouteurs pour une meilleure immersion.</li>
        <li>🛋️ Un endroit calme et propice à la relaxation.</li>
      </ul>
      <p>
        Votre <strong>bien-être</strong> est ma priorité. En cas d'imprévu
        technique, nous trouverons ensemble un nouvel horaire.
      </p>
    </section>

    <section class="section-cta">
      <h2>
        Prêt(e) à vous libérer du <strong>stress</strong> et atteindre vos
        objectifs grâce à l'<strong>hypnose</strong> ?
      </h2>
      <p>
        Contactez-moi dès aujourd'hui pour planifier votre première
        <strong>séance d'hypnose</strong> personnalisée.
      </p>

      <div class="booking-info">
        <p>
          Après validation du rendez-vous, vous recevrez un mail avec le lien
          Google Meet et un lien de paiement sécurisé.
        </p>
        <p>
          <strong class="attention-text">
            Connectez-vous 5 minutes avant la séance pour un démarrage serein.
          </strong>
        </p>
      </div>
    </section>
  </main>
</template>

<style scoped>
/* Les styles restent majoritairement les mêmes, sauf pour p et li text-align */

/* Styles généraux */
.container {
  font-family: "Yuji Syuku", serif;
  width: 90%;
  max-width: 800px;
  margin: auto;
  font-size: 1em;
  line-height: 1.6;
  padding: 20px 0;
}

/* Styles pour le texte en gras */
strong {
  color: rgb(100, 50, 180);
}

/* Animation titre */
.typed-heading {
  font-size: 1.8em;
  text-align: center;
  color: #000;
  border-right: 2px solid black;
  white-space: nowrap;
  overflow: hidden;
  display: inline-block;
  width: max-content;
  animation: blinkCursor 0.8s infinite step-end;
  margin-bottom: 1em;
}

/* Amélioration de l'animation du curseur */
@keyframes blinkCursor {
  50% {
    border-color: transparent;
  }
}

/* Titres */
h2 {
  font-size: 1.6em;
  color: #000;
  margin-top: 2em;
  margin-bottom: 0.8em;
  position: relative;
  text-align: center;
}

/* Effet soulignement sur h2 */
h2::after {
  content: "";
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  bottom: -8px;
  width: 0;
  height: 2px;
  background-color: rgb(135, 89, 210);
  transition: width 0.4s ease-out;
}

h2:hover::after {
  width: 70%;
}

/* Paragraphes et listes */
p {
  font-size: 1em;
  text-align: justify; /* MODIFIÉ : Revertir à 'justify' ou 'left' pour la lisibilité */
  margin-bottom: 1em;
}

ul {
  list-style: none;
  padding: 0;
  margin: 1em 0;
}

li {
  text-align: left; /* MODIFIÉ : Revertir à 'left' pour la lisibilité */
  margin-bottom: 0.5em;
  font-size: 1em;
}

/* Séparateur */
.separator {
  border: none;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  margin: 3em 0;
}

/* Liens génériques */
.link-more-info {
  display: block;
  text-align: center;
  color: rgb(135, 89, 210);
  text-decoration: none;
  margin-top: 1em;
  transition: color 0.2s ease-in-out, font-size 0.2s ease-in-out;
}

.link-more-info:hover {
  text-decoration: underline;
  font-size: 1.05em;
  color: rgba(135, 89, 210, 0.8);
}

/* Bouton principal (ex: prendre RDV) */
.button-primary {
  display: block;
  text-align: center;
  background-color: rgb(135, 89, 210);
  color: white;
  padding: 0.9em 1.8em;
  border-radius: 0.5em;
  text-decoration: none;
  font-weight: bold;
  margin-top: 1.5em;
  transition: background-color 0.3s ease, transform 0.2s ease;
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
}

.button-primary:hover {
  background-color: rgba(135, 89, 210, 0.8);
  transform: translateY(-2px);
}

/* Bloc tarif */
.tarif-box {
  width: 90%;
  max-width: 450px;
  text-align: center;
  padding: 1.5em;
  margin: 2em auto;
  background-color: white;
  box-shadow: 0 0.5em 1.5em rgba(0, 0, 0, 0.1);
  border-radius: 0.8em;
  font-size: 1.05em;
  transition: transform 0.3s ease-in-out;
}

.tarif-box:hover {
  transform: scale(1.02);
}

/* Section finale */
.section-cta {
  text-align: center;
  margin-top: 3em;
}

.booking-info {
  text-align: center;
  margin-top: 1.5em;
  padding: 1em;
  background-color: #f9f9f9;
  border-radius: 0.5em;
}

.attention-text {
  color: rgb(135, 89, 210);
  font-size: 1.1em;
  font-weight: bold;
}

/* Responsive */
@media (max-width: 768px) {
  .container {
    width: 95%;
    padding: 10px 0;
  }
  .typed-heading {
    font-size: 1.5em;
  }
  h2 {
    font-size: 1.4em;
    margin-top: 1.5em;
  }
  p,
  li {
    font-size: 0.95em;
    text-align: left; /* MODIFIÉ : Revertir à 'left' pour la lisibilité sur mobile aussi */
  }
  .link-more-info,
  .button-primary {
    font-size: 0.95em;
  }
  .tarif-box {
    width: 95%;
    font-size: 0.95em;
  }
  .separator {
    margin: 2em 0;
  }
}
</style>

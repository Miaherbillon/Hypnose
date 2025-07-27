<script setup>
import { ref, onMounted, onUnmounted } from "vue";

// Animation machine à écrire pour le titre
const typedText = ref("");
// Texte plus optimisé avec mots-clés ciblés
const fullText =
  "Hypnose Elmanienne à Besançon - Séances en ligne pour votre bien-être";
let index = 0;
let interval = null;

onMounted(() => {
  interval = setInterval(() => {
    typedText.value = fullText.slice(0, index);
    index++;
    if (index > fullText.length) clearInterval(interval);
  }, 100);
});

onUnmounted(() => {
  if (interval) clearInterval(interval);
});
</script>

<template>
  <section class="container">
    <h1 aria-live="polite">{{ typedText }}</h1>

    <section>
      <h2>Votre praticienne en hypnose à Besançon et en ligne</h2>
      <p>Je suis Mia, votre praticienne certifiée en hypnose Elmanienne.</p>
      <p>
        Formée par l’école suisse Omni depuis 2020, je vous accompagne avec
        bienveillance dans votre cheminement vers un meilleur **bien-être**
        personnel, que vous soyez à **Besançon**, en région Franche-Comté, ou
        partout en France grâce aux séances en ligne.
      </p>
      <p>
        L’hypnose est une rencontre avec soi-même, un espace où l’on peut se
        reconnecter à son potentiel et amorcer de véritables transformations
        pour retrouver sérénité et équilibre. ✨
      </p>
    </section>

    <hr />

    <section>
      <h2>Démystifions l'hypnose : Reprendre le contrôle de soi</h2>
      <p>
        <strong>
          Contrairement aux idées reçues et aux clichés, l'hypnose ne consiste
          pas à perdre le contrôle, mais au contraire à reprendre le pouvoir sur
          soi-même en accédant aux ressources cachées de l’inconscient. C'est un
          état naturel de conscience modifiée, propice au changement.
        </strong>
      </p>
    </section>

    <hr />

    <section>
      <h2>Les bienfaits de l'hypnose pour votre bien-être</h2>
      <p>
        Nos émotions façonnent nos perceptions, nos décisions et nos réactions
        face aux événements de la vie. Parfois, elles peuvent nous submerger ou
        nous bloquer, notamment lorsqu’elles sont liées à des traumatismes
        passés, à des peurs ou à des schémas répétitifs. L'hypnose offre une
        approche douce et efficace pour naviguer ces défis.
      </p>
      <p>
        <strong
          >Grâce à l’hypnose, il est possible de retrouver un profond
          **bien-être** en :</strong
        >
      </p>
      <ul>
        <li>✅ Comprenant et libérant des émotions refoulées</li>
        <li>
          💪 Dépassant des blocages et des peurs (phobies, anxiété, stress)
        </li>
        <li>
          🧘‍♀️ Se libérant des croyances limitantes pour une meilleure estime de
          soi et une confiance retrouvée
        </li>
        <li>😴 Améliorant la qualité de votre sommeil</li>
        <li>🚬 Gérant les addictions (arrêt du tabac, etc.)</li>
        <li>
          🤕 Soulageant certaines douleurs chroniques (en complément médical)
        </li>
      </ul>
      <p>
        Que vous cherchiez à **Besançon** ou ailleurs une aide pour le stress,
        l'anxiété ou le sommeil, l'hypnose peut être un chemin vers la solution.
      </p>
    </section>

    <hr />

    <section>
      <h2>Qu'est-ce que l'hypnose Elmanienne ? Une méthode efficace</h2>
      <p>
        L'hypnose Elmanienne est une technique rapide et directe, axée sur
        l'atteinte d'un état d'hypnose profonde pour faciliter le travail
        thérapeutique. Elle est réputée pour son efficacité dans la résolution
        de problématiques spécifiques et le renforcement des ressources
        personnelles.
      </p>
      <a href="#info" class="link"
        >Cliquez ici pour en savoir plus sur cette approche d'hypnose</a
      >
    </section>

    <section>
      <h2>Déroulement des séances d'hypnose en ligne</h2>
      <p>
        Je vous propose des séances d'hypnose d'une heure, en toute sérénité et
        **à distance via Google Meet**, pour vous permettre de bénéficier de mes
        services où que vous soyez, y compris si vous êtes à **Besançon** et
        préférez le confort de votre domicile.
      </p>

      <div class="tarif">
        <p>💰 **Tarif : 70 euros la séance d'hypnose**</p>
        <p>
          Prenez rendez-vous en ligne ci-dessous pour votre séance de
          **bien-être**.
        </p>
        <a href="#votre-lien-de-rdv" class="link-button"
          >Prendre rendez-vous en ligne</a
        >
      </div>
    </section>

    <section>
      <h2>Comment bien se préparer à une séance d'hypnose à distance ?</h2>
      <p>
        <strong
          >Pour une séance réussie et une expérience optimale, prévoyez
          :</strong
        >
      </p>
      <ul>
        <li>✅ Une connexion internet stable</li>
        <li>🎧 Un casque ou des écouteurs pour une meilleure immersion</li>
        <li>
          🛋️ Un endroit calme et propice à la relaxation, où vous ne serez pas
          dérangé(e)
        </li>
      </ul>
      <p>
        En cas de problème technique lors de votre séance à distance, nous
        conviendrons ensemble d'un nouvel horaire, votre **bien-être** est ma
        priorité !
      </p>
    </section>

    <section class="final-section">
      <h2>
        Prêt(e) à vous libérer du stress, améliorer votre bien-être et atteindre
        vos objectifs grâce à l'hypnose ?
      </h2>
      <p>
        Contactez-moi dès aujourd'hui pour prendre rendez-vous pour une séance
        d'hypnose.
      </p>

      <div class="validation">
        <p>
          Après validation du rendez-vous pour votre séance d'hypnose, vous
          recevrez un mail avec le lien de connexion Google Meet ainsi qu'un
          lien de paiement en ligne sécurisé.
        </p>
        <p>
          <strong class="highlight"
            >Merci de vous connecter 5 minutes avant le début de la séance pour
            un démarrage serein.</strong
          >
        </p>
      </div>
    </section>
  </section>
</template>

<style scoped>
/* Les styles restent globalement les mêmes, mais vous pourriez ajuster pour le nouveau bouton */
/* Styles généraux */
.container {
  font-family: "Yuji Syuku", serif;
  width: 90%;
  max-width: 800px;
  margin: auto;
  font-size: 1em;
  line-height: 1.6;
}

/* Animation titre */
h1 {
  font-size: 1.5em;
  text-align: center;
  color: #000;
  border-right: 2px solid black;
  white-space: nowrap;
  overflow: hidden;
  display: inline-block;
  width: max-content;
  animation: blinkCursor 0.8s infinite step-end;
}

/* Amélioration de l'animation du curseur */
@keyframes blinkCursor {
  50% {
    border-color: transparent;
  }
}

/* Titres */
h2 {
  font-size: 1.5em;
  color: #000;
  margin-top: 1.5em;
  position: relative;
}

/* Effet soulignement sur h2 */
h2::after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: -5px;
  width: 0;
  height: 2px;
  background-color: rgb(135, 89, 210);
  transition: width 0.4s ease-out, left 0.4s ease-out;
}

h2:hover::after {
  width: 100%;
  left: 0;
}

/* Paragraphes et listes */
p {
  font-size: 1em;
  text-align: center;
}

/* Boutons et liens */
.link {
  text-decoration: none;
  color: rgb(135, 89, 210);
  display: block;
  text-align: center;
  transition: color 0.2s ease-in-out;
}

.link:hover {
  text-decoration: underline;
  font-size: 1.05em;
  color: rgba(135, 89, 210, 0.8);
}

.link-button {
  /* Nouveau style pour le bouton de RDV */
  display: block;
  text-align: center;
  background-color: rgb(135, 89, 210);
  color: white;
  padding: 0.8em 1.5em;
  border-radius: 0.5em;
  text-decoration: none;
  font-weight: bold;
  margin-top: 1em;
  transition: background-color 0.3s ease;
}

.link-button:hover {
  background-color: rgba(135, 89, 210, 0.8);
}

/* Bloc tarif */
.tarif {
  width: 90%;
  max-width: 400px;
  text-align: center;
  padding: 1em;
  margin: 1.5em auto;
  background-color: white;
  box-shadow: 0 0.3em 1em rgba(0, 0, 0, 0.5);
  border-radius: 0.8em;
  font-size: 1em;
  transition: transform 0.3s ease-in-out;
}

.tarif:hover {
  transform: scale(1.05);
}

/* Section finale */
.final-section {
  text-align: center;
  margin-top: 1.5em;
}

.validation {
  text-align: center;
  margin-top: 1em;
}

.highlight {
  color: rgb(135, 89, 210);
  font-size: 1.1em;
}

/* Responsive */
@media (max-width: 768px) {
  h1 {
    font-size: 1.2em;
  }
  h2 {
    font-size: 1.3em;
  }
  p,
  li {
    font-size: 0.9em;
  }
  .link,
  .link-button {
    font-size: 1em;
  }
  .tarif {
    width: 100%;
    font-size: 0.9em;
  }
}
</style>

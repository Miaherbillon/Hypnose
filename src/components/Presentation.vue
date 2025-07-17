<script setup>
import { ref, onMounted, onUnmounted } from "vue";

// Animation machine à écrire pour le titre
const typedText = ref("");
const fullText = "Hypnose Elmanienne - Séances en ligne";
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
      <h2>Présentation</h2>
      <p>Mia, votre praticienne en hypnose Elmanienne.</p>
      <p>
        Formée par l’école suisse Omni depuis 2020, je vous accompagne avec
        bienveillance dans votre cheminement personnel.
      </p>
      <p>
        L’hypnose est une rencontre avec soi-même, un espace où l’on peut se
        reconnecter à son potentiel et amorcer de véritables transformations. ✨
      </p>
    </section>

    <hr />

    <section>
      <h2>Une idée reçue sur l'hypnose</h2>
      <p>
        <strong>
          Contrairement aux idées reçues, l'hypnose ne consiste pas à perdre le
          contrôle, mais au contraire à reprendre le pouvoir sur soi-même en
          accédant aux ressources cachées de l’inconscient.
        </strong>
      </p>
    </section>

    <hr />

    <section>
      <h2>Les bienfaits de l'hypnose</h2>
      <p>
        Nos émotions façonnent nos perceptions, nos décisions et nos réactions
        face aux événements de la vie. Parfois, elles peuvent nous submerger ou
        nous bloquer, notamment lorsqu’elles sont liées à des traumatismes
        passés, à des peurs ou à des schémas répétitifs.
      </p>
      <p><strong>Grâce à l’hypnose, il est possible de :</strong></p>
      <ul>
        <li>✅ Comprendre et libérer des émotions refoulées</li>
        <li>💪 Dépasser des blocages et des peurs</li>
        <li>
          🧘‍♀️ Se libérer des croyances limitantes pour une meilleure estime de
          soi
        </li>
      </ul>
    </section>

    <hr />

    <section>
      <h2>Qu'est-ce que l'hypnose Elmanienne ?</h2>
      <a href="#info" class="link">Cliquez ici pour en savoir plus</a>
    </section>

    <section>
      <h2>Déroulement des séances</h2>
      <p>
        Je vous propose des séances d'hypnose d'une heure, en toute sérénité et
        à distance via Google Meet.
      </p>

      <div class="tarif">
        <p>💰 70 euros la séance</p>
        <p>Prenez rendez-vous en ligne ci-dessous.</p>
      </div>
    </section>

    <section>
      <h2>Comment bien se préparer ?</h2>
      <p><strong>Pour une séance réussie, prévoyez :</strong></p>
      <ul>
        <li>✅ Une connexion internet stable</li>
        <li>🎧 Un casque ou des écouteurs</li>
        <li>🛋️ Un endroit calme et propice à la relaxation</li>
      </ul>
      <p>
        En cas de problème technique lors de votre séance à distance, nous
        conviendrons ensemble d'un nouvel horaire, restons zen !
      </p>
    </section>

    <section class="final-section">
      <h2>Prêt(e) à vous libérer du stress et à atteindre vos objectifs ?</h2>
      <p>Contactez-moi pour prendre rendez-vous.</p>

      <div class="validation">
        <p>
          Après validation du rendez-vous, vous recevrez un mail avec le lien de
          connexion Google Meet ainsi qu'un lien de paiement en ligne sécurisé.
        </p>
        <p>
          <strong class="highlight"
            >Merci de vous connecter 5 minutes avant le début de la
            séance.</strong
          >
        </p>
      </div>
    </section>
  </section>
</template>

<style scoped>
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
  .link {
    font-size: 1em;
  }
  .tarif {
    width: 100%;
    font-size: 0.9em;
  }
}
</style>

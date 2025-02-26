<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="P">
    <h1>Hypnose Elmanienne - Séances en ligne</h1>

    <h2>Présentation</h2>
    <p class="O">Mia, votre praticienne en hypnose Elmanienne.</p>
    <p class="O">
      Formée par l’école suisse Omni depuis 2020, je vous accompagne avec
      bienveillance dans votre cheminement personnel.
    </p>

    <p class="O">
      L’hypnose est une rencontre avec soi-même, un espace où l’on peut se
      reconnecter à son potentiel et amorcer de véritables transformations. ✨
    </p>

    <hr />

    <h2>Une idée reçue sur l'hypnose</h2>
    <p>
      <strong>
        Contrairement aux idées reçues, l'hypnose ne consiste pas à perdre le
        contrôle, mais au contraire à reprendre le pouvoir sur soi-même en
        accédant aux ressources cachées de l’inconscient.
      </strong>
    </p>

    <hr />

    <h2>Les bienfaits de l'hypnose</h2>
    <p>
      Nos émotions façonnent nos perceptions, nos décisions et nos réactions
      face aux événements de la vie. Parfois, elles peuvent nous submerger ou
      nous bloquer, notamment lorsqu’elles sont liées à des traumatismes passés,
      à des peurs ou à des schémas répétitifs.
    </p>

    <p><strong>Grâce à l’hypnose, il est possible de :</strong></p>
    <ul>
      <li>✅ Comprendre et libérer des émotions refoulées</li>
      <li>💪 Dépasser des blocages et des peurs</li>
      <li>
        🧘‍♀️ Se libérer des croyances limitantes pour une meilleure estime de soi
      </li>
    </ul>

    <hr />

    <p class="O">
      Ces pensées profondément ancrées influencent nos choix de vie et nos
      comportements. L’hypnose permet de les déconstruire et de les remplacer
      par des croyances plus aidantes.
    </p>

    <hr />

    <h2>Qu'est-ce que l'hypnose Elmanienne ?</h2>
    <a href="#info" class="Q">Cliquez ici pour en savoir plus</a>

    <h2>Déroulement des séances</h2>
    <p>
      Je vous propose des séances d'hypnose d'une heure, en toute sérénité et à
      distance via Google Meet.
    </p>

    <div class="tarif">
      <p>💰 60 euros la séance</p>
      <p>Prenez rendez-vous en ligne ci-dessous.</p>
    </div>

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

    <h2>Prêt(e) à vous libérer du stress et à atteindre vos objectifs ?</h2>
    <p>Contactez-moi pour prendre rendez-vous.</p>

    <div class="V">
      <p>
        Après validation du rendez-vous, vous recevrez un mail avec le lien de
        connexion Google Meet ainsi qu'un lien de paiement en ligne sécurisé.
      </p>
      <p>
        <strong class="S"
          >Merci de vous connecter 5 minutes avant le début de la
          séance.</strong
        >
      </p>
    </div>
  </div>
</template>

<style scoped>
/* Styles généraux */
.P {
  font-family: "Yuji Syuku", serif;
  width: 90%;
  max-width: 800px;
  margin: auto;
  font-size: 1em;
  line-height: 1.6;
}

/* Titres */
h1 {
  font-size: 1.5em;
  text-align: center;
  color: #000;
}
h2 {
  font-size: 1.5em;
  color: #000;
  margin-top: 1.5em;
}
h3 {
  font-size: 1.3em;
  margin-top: 1em;
}

/* Paragraphes et listes */
p {
  font-size: 1em;
  text-align: center;
  margin: 1em 0;
}
ul {
  list-style: none;
  padding: 0;
  text-align: center;
}
li {
  font-size: 1em;
  margin: 0.5em 0;
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
}

/* Liens */
.Q {
  text-decoration: none;
  color: rgb(135, 89, 210);
  display: block;
  text-align: center;
  font-size: 1.1em;
  margin-top: 1.5em;
}
a.Q:hover {
  text-decoration: underline;
  font-size: 1.15em;
}

/* Section finale */
.V {
  text-align: center;
  margin-top: 1.5em;
}
.S {
  color: rgb(135, 89, 210);
  font-size: 1.1em;
}

/* 📱 Responsive */
@media (max-width: 768px) {
  h1 {
    font-size: 1em;
  }
  h2 {
    font-size: 0.8em;
  }
  h3 {
    font-size: 0.8em;
  }
  p,
  li {
    font-size: 0.7em;
  }
  .tarif {
    width: 90%;
    font-size: 0.9em;
  }
  .Q {
    font-size: 0.8em;
  }
  a {
    font-size: 0.8em;
  }
}
</style>

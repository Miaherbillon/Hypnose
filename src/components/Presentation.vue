<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="P">
    <h2>Présentation</h2>
    <div>
      <p class="O">Mia, votre praticienne en hypnose Elmanienne.</p>
      <p class="O">
        Formée par l’école suisse Omni depuis 2020 , je vous accompagne avec
        bienveillance dans votre cheminement personnel.
      </p>

      <p class="O">
        L’hypnose est une rencontre avec soi-même, un espace où l’on peut se
        reconnecter à son potentiel et amorcer de véritables transformations. ✨
      </p>
      <p class="O">________________________</p>
      <p>
        <strong class="Q">
          Contrairement aux idées reçues, l'hypnose ne consiste pas à perdre le
          contrôle, mais au contraire à reprendre le pouvoir sur soi-même en
          accédant aux ressources cachées de l’inconscient.
        </strong>
      </p>
      <p class="O">________________________</p>
      <p>
        Nos émotions façonnent nos perceptions, nos décisions et nos réactions
        face aux événements de la vie. Parfois, elles peuvent nous submerger ou
        nous bloquer, notamment lorsqu’elles sont liées à des traumatismes
        passés, à des peurs ou à des schémas répétitifs.
      </p>
      <p><strong>Grâce à l’hypnose, il est possible de :</strong></p>
      <p>- Comprendre et libérer des émotions refoulées.</p>
      <p>- Dépasser des blocages et des peurs.</p>
      <p>
        - Se libérer des croyances limitantes pour une meilleur estime de soi.
      </p>
      <p class="O">________________________</p>
      <p class="O">
        Ces pensées profondément ancrées influencent nos choix de vie et nos
        comportements. L’hypnose permet de les déconstruire et de les remplacer
        par des croyances plus aidantes.
      </p>
      <p class="O">________________________</p>

      <a href="#info" class="Q">C'est quoi l'hypnose Elmanienne ?</a>

      <p></p>
      <p>
        Je vous propose des séances d'hypnose d'une heure, en toute sérénité et
        à distance via Google Meet.
        <strong class="tarif">
          60 euros la séance
          <br />
          Prenez rendez-vous en ligne ci-dessous.
        </strong>
      </p>

      <p><strong>Pour une séance réussie, prévoyez :</strong></p>
      <ul>
        <li>Une connexion internet stable</li>
        <li>Un casque ou des écouteurs</li>
        <li>Un endroit calme et propice à la relaxation</li>
      </ul>
      <p>
        En cas de problème technique lors de votre séance à distance, nous
        conviendrons ensemble d'un nouvel horaire, restons zen !
      </p>
      <p>
        <strong>
          Prêt(e) à vous libérer du stress et à atteindre vos objectifs ?
        </strong>
        <br />
        Contactez-moi pour prendre rendez-vous.
      </p>
      <br />
      <div class="V">
        <p>
          Après validation du rendez-vous, vous recevrez un mail avec le lien de
          connexion Google Meet ainsi qu'un lien de paiement en ligne sécurisé.
        </p>

        <p>
          <strong class="S">
            Merci de vous connecter 5 minutes avant le début de la séance.
          </strong>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped>
strong {
  text-decoration: underline;
}
.P {
  /* font-family: "Cutive Mono", serif; */
  font-family: "Yuji Syuku", serif;
  width: 80%;
  /* padding: 2em 4em; */
  margin: auto;
  font-size: 1em;
}
.D {
  color: rgb(135, 89, 210);
  display: flex;
  justify-content: center;
  font-size: 1.2em;
  /* margin: 1em 0; */
}
h2 {
  color: #000000;
  font-size: 2em;
  text-align: center;
}

.tarif {
  width: 60%;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 2em;
  text-align: center;
  padding: 1em;
  margin: 2em auto;
  background-color: white;
  overflow: hidden;
  box-shadow: 0 0.5em 1.5em 0 rgba(0, 0, 0, 0.6);
  transform: translateY(0px);
  animation: float 6s ease-in-out infinite;
}
.O {
  text-decoration: none;
  color: rgb(0, 0, 0);
  display: flex;
  justify-content: center;
  font-size: 1em;
  margin: 1.4em 0;
  text-align: center;
}
.Q {
  text-decoration: none;
  color: rgb(135, 89, 210);
  display: flex;
  justify-content: center;
  font-size: 1.1em;
  margin: 1.4em 0;
  transition: text-decoration 0.3s ease-in-out;
  text-align: center;
}
a.Q:hover {
  text-decoration: underline;
  font-size: 1.3em;
}
.V {
  width: 100%;
  margin: auto;
  text-align: center;
}
.S {
  color: rgb(135, 89, 210);
  text-decoration: none;
  font-size: 1.2em;
}

/* 📱 Responsive pour les téléphones */
@media (max-width: 768px) {
  h2 {
    font-size: 1em;
  }

  p {
    font-size: 0.8em;
  }
  .tarif {
    width: 80%;
    font-size: 1em;
    padding: 1em;
    font-size: 0.8em;
  }
  .O {
    margin: 0.5em auto;
    font-size: 0.8em;
  }

  .Q {
    margin: 1.5em 0;
    font-size: 0.8em;
  }
  a.Q:hover {
    font-size: 1em;
  }

  .D {
    font-size: 1em;
    text-align: center;
    font-size: 0.8em;
  }
  .S {
    font-size: 1em;
  }

  ul {
    padding-left: 1em;
  }

  li {
    font-size: 0.8em;
  }
  .tarif {
    font-size: 1em;
    text-decoration: none;
  }
}
</style>

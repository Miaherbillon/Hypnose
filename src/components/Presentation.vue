<script setup>
import { ref } from "vue";
</script>

<template>
  <div class="P">
    <h2>Présentation</h2>
    <div>
      <p><strong>Mia, votre praticienne en hypnose Elmanienne</strong></p>
      <p>
        Formée par l'école suisse Omni depuis 2020, je vous accompagne dans
        votre bien-être grâce à l'hypnose.
      </p>
      <a href="#contact" class="Q">C'est quoi l'hypnose Elmanienne ?</a>

      <p>
        <strong>
          Séances personnalisées à distance ou à domicile
          (Bourgogne-Franche-Comté)
        </strong>
      </p>
      <p>
        Je vous propose des séances d'hypnose d'une heure, en toute sérénité,
        directement chez vous ou à distance via Zoom.
        <strong class="tarif">
          60 euros la séance
          <br />
          Prenez rendez-vous en ligne ci-dessous.
        </strong>
      </p>
      <p class="D">
        Si déplacement à domicile, prenez rendez-vous directement par mail :
        mhypnose25@gmail.com
      </p>

      <p><strong>Pour une séance réussie, prévoyez :</strong></p>
      <ul>
        <li>Une connexion internet stable</li>
        <li>Un casque ou des écouteurs</li>
        <li>Un endroit calme et propice à la relaxation</li>
      </ul>
      <p>
        En cas de problème technique lors de votre séance à distance, nous
        conviendrons ensemble d'un nouvel horaire.
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
        Après validation du rendez-vous, vous recevrez un mail avec le lien de
        connexion Google Meet ainsi qu'un lien de paiement en ligne sécurisé.
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
/* Styles de base */
.P {
  width: 70%;
  padding: 2em 4em;
  margin: auto;
}
.D {
  color: rgb(210, 89, 194);
  display: flex;
  justify-content: center;
  font-size: 1.2em;
  margin: 2em 0;
}
h2 {
  color: #000000;
  -webkit-text-stroke: rgba(0, 0, 0, 0.229) 0.08em;
  font-size: 2em;
  text-align: center;
}
strong {
  color: #000000;
  font-size: 1.2em;
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
.Q {
  text-decoration: none;
  color: rgb(210, 89, 194);
  display: flex;
  justify-content: center;
  font-size: 1.5em;
  margin: 2em 0;
  transition: text-decoration 0.3s ease-in-out;
  text-align: center;
}
.Q:hover {
  text-decoration: underline;
}
.V {
  width: 100%;
  margin: auto;
  text-align: center;
}
.S {
  color: rgb(210, 89, 194);
}

/* 📱 Responsive pour les téléphones */
@media (max-width: 768px) {
  .P {
    width: 80%;
    margin: auto;
  }

  h2 {
    font-size: 1.5em;
  }

  strong {
    font-size: 1em;
  }

  .tarif {
    width: 80%;
    font-size: 1em;
    padding: 1em;
  }

  .Q {
    font-size: 1.2em;
    margin: 1.5em 0;
  }

  .D {
    font-size: 1em;
    text-align: center;
  }

  ul {
    padding-left: 1em;
  }

  li {
    font-size: 1em;
  }
}
</style>

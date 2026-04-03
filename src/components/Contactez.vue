<script setup>
// Pas de logique complexe ici, juste un lien mailto
</script>

<template>
  <section class="contact-container" id="contact">
    <div class="contact-card">
      <h2 class="section-title">Une question ?</h2>
      <p class="contact-intro">
        👋 N’hésitez pas à m’écrire, je vous répondrai avec plaisir !
      </p>

      <a href="mailto:mhypnose25@gmail.com" class="button-primary">
        ✉️ Envoyez-moi un mail
      </a>

      <p class="contact-subtext">mhypnose25@gmail.com</p>
    </div>
  </section>
</template>

<style scoped>
.contact-container {
  padding: 0;
  max-width: 1000px;
  margin: 40px auto;
}

.contact-card {
  font-family: "Quicksand", sans-serif;
  background: #ffffffa5;
  padding: 40px 25px;
  border-radius: 40px;
  box-shadow: 0 15px 35px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
  text-align: center;
}

/* On utilise le même style de titre que les autres sections */
.section-title {
  font-family: "Playfair Display", serif;
  font-size: 1.8em;
  color: #000000;
  margin-bottom: 15px;
}

.contact-intro {
  font-size: 1.1em;
  color: #666;
  margin-bottom: 25px;
}

.contact-subtext {
  margin-top: 15px;
  font-size: 0.9em;
  color: #9d80cb;
  font-weight: 500;
}

/* Bouton harmonisé avec ton CTA de réservation */
.button-primary {
  display: inline-block;
  background: linear-gradient(135deg, #9d80cb, #8265b5);
  color: white;
  padding: 15px 35px;
  border-radius: 50px;
  text-decoration: none;
  font-weight: 700;
  transition: all 0.3s ease;
  box-shadow: 0 8px 20px rgba(157, 128, 203, 0.2);
}

.button-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 12px 25px rgba(157, 128, 203, 0.3);
  filter: brightness(1.1);
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .contact-card {
    padding: 30px 15px;
    border-radius: 30px;
    margin: 0 10px;
  }

  .section-title {
    font-size: 1.4em !important;
  }

  .contact-intro {
    font-size: 0.95em;
  }

  .button-primary {
    font-size: 0.9em;
    padding: 12px 25px;
  }
}
</style>

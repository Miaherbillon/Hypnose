<script setup>
// Utilisation de la version moderne <script setup> comme le reste de ton site
</script>

<template>
  <section class="calendar-section" id="votre-lien-de-rdv">
    <div class="calendar-card">
      <h2 class="section-title">Réserver votre séance</h2>
      <p class="calendar-instruction">
        Choisissez le créneau qui vous convient directement ci-dessous :
      </p>

      <div class="iframe-container">
        <iframe
          src="https://calendar.google.com/calendar/appointments/schedules/AcZssZ2D_EGei9t_KNaPrUTl5R9MXfXoJuNARyZck-xfZ90PG01w5ny46P1BGTVEs9UiO7qWdbafnw_9?gv=true"
          class="calendar-iframe"
          frameborder="0"
          scrolling="yes">
        </iframe>
      </div>
    </div>
  </section>
</template>

<style scoped>
.calendar-section {
  padding: 0;
  max-width: 1000px;
  margin: 40px auto;
}

.calendar-card {
  font-family: "Quicksand", sans-serif;
  background: #ffffffa5;
  padding: 40px 20px;
  border-radius: 40px;
  box-shadow: 0 15px 35px rgba(135, 89, 210, 0.05);
  border: 1px solid rgba(135, 89, 210, 0.1);
  text-align: center;
}

.section-title {
  font-family: "Playfair Display", serif;
  font-size: 1.8em;
  color: #000000;
  margin-bottom: 10px;
}

.calendar-instruction {
  font-size: 1.05em;
  color: #666;
  margin-bottom: 30px;
}

/* Conteneur pour l'iframe pour gérer le scroll proprement */
.iframe-container {
  width: 100%;
  overflow: hidden;
  border-radius: 20px;
  background: white;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.03);
}

.calendar-iframe {
  width: 100%;
  height: 700px; /* Hauteur fixe pour éviter les bugs d'affichage */
  border: none;
}

/* --- RESPONSIVE MOBILE --- */
@media (max-width: 768px) {
  .calendar-card {
    padding: 25px 10px;
    border-radius: 30px;
    margin: 0 5px;
  }

  .section-title {
    font-size: 1.4em !important;
  }

  .calendar-instruction {
    font-size: 0.9em;
    padding: 0 10px;
  }

  .calendar-iframe {
    height: 600px; /* Un peu plus court sur mobile */
  }
}
</style>

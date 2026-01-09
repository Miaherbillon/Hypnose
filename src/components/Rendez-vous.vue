<template>
  <div class="calendrier" id="votre-lien-de-rdv">
    <iframe
      src="https://calendar.google.com/calendar/appointments/schedules/AcZssZ2D_EGei9t_KNaPrUTl5R9MXfXoJuNARyZck-xfZ90PG01w5ny46P1BGTVEs9UiO7qWdbafnw_9?gv=true"
      class="calendar-iframe"
      frameborder="0"></iframe>
  </div>
</template>

<script>
export default {
  data() {
    return {
      calendarUrl:
        "https://calendar.google.com/calendar/embed?src=herbillon.mia%40gmail.com&ctz=Europe%2FBrussels",
    };
  },
};
</script>

<style scoped>
.calendrier {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 80%;
  margin: auto;
  background: #ffffffa5;
}

.calendar-iframe {
  width: 80vw; /* Largeur à 80% de l'écran */
  height: 70vh; /* Hauteur à 80% de la hauteur de l'écran */
  max-width: 1200px; /* Largeur maximale */
  max-height: 800px; /* Hauteur maximale */
  border: none;
  box-shadow: 0 20px 50px rgba(135, 89, 210, 0.12);
}

@media (max-width: 880px) {
  .calendar-iframe {
    width: 80vw; /* Plus large sur petits écrans */
    height: 70vh; /* Réduit légèrement la hauteur */
  }
}

@media (max-width: 480px) {
  .calendar-iframe {
    width: 80vw;
    height: 60vh;
  }
}
</style>

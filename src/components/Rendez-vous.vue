<template>
  <div class="calendrier">
    <iframe
      src="https://calendar.google.com/calendar/appointments/schedules/AcZssZ2D_EGei9t_KNaPrUTl5R9MXfXoJuNARyZck-xfZ90PG01w5ny46P1BGTVEs9UiO7qWdbafnw_9?gv=true"
      style="border: 0"
      width="100%"
      height="600"
      frameborder="0"></iframe>
  </div>
</template>

<script>
export default {
  data() {
    return {
      calendarUrl:
        "https://calendar.google.com/calendar/embed?src=herbillon.mia%40gmail.com&ctz=Europe%2FBrussels",
      calendarWidth: "100vw",
      calendarHeight: "50vh",
    };
  },
};
</script>
<style scoped></style>

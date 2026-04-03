<script setup></script>

<template>
  <div class="title-wrapper">
    <img src="/logo2.png" alt="Logo" class="Logo" />
    <h2 class="main-title">Séances d'hypnose OMNI & Elmanienne en visio</h2>
    <div class="icon-container">
      <FontAwesomeIcon
        icon="fa-solid fa-arrow-down-long"
        beat
        class="arrow-icon" />
    </div>
  </div>
</template>

<style scoped>
.title-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 1em auto 1em auto;
  width: 100%;
}

.main-title {
  font-family: "Playfair Display", serif;
  font-size: 2em;
  color: #000000;
  background-color: white;
  padding: 0.2em 1.2em;
  border-radius: 100px;
  box-shadow: 0 10px 30px rgba(157, 128, 203, 0.15);
  border: 4px solid white;
  text-align: center;
  margin: 0;
}

.icon-container {
  margin-top: 1.5em;
}

.arrow-icon {
  color: #9d80cb;
  font-size: 1.5em;
}
.Logo {
  width: 30em;
}
@media (max-width: 768px) {
  .main-title {
    font-size: 1em;
    padding: 0.3em 1.2em;
    border-radius: 40px;
    border-width: 2px;
  }
  /* .title-wrapper {
    margin: 0.5em auto 1.5em auto;
  } */
}
</style>

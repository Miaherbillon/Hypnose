<script setup>
import { ref } from "vue";
const isOpen = ref(false);
</script>

<template>
  <div class="menu-system" :class="{ active: isOpen }">
    <button class="trigger" @click="isOpen = !isOpen" aria-label="Menu">
      <div class="burger">
        <span></span>
        <span></span>
      </div>
    </button>

    <nav class="dropdown">
      <a href="#votre-lien-de-rdv" @click="isOpen = false">RÉSERVATION</a>
      <div class="divider"></div>
      <a href="#contact" @click="isOpen = false">CONTACT</a>
    </nav>

    <div v-if="isOpen" class="closer" @click="isOpen = false"></div>
  </div>
</template>
<style scoped>
.menu-system {
  /* Fixe le composant par rapport à la fenêtre, pas au contenu */
  position: fixed;
  top: 20px;
  right: 20px;
  z-index: 10000;
  /* Empêche toute interaction en dehors du bouton quand fermé */
  pointer-events: none;
}

.trigger {
  pointer-events: auto; /* Réactive le clic sur le bouton */
  width: 44px;
  height: 44px;
  border-radius: 50%;
  background: white;
  border: 1px solid rgba(157, 128, 203, 0.2);
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
  float: right; /* Aligne le bouton à droite du conteneur */
}

.burger span {
  display: block;
  width: 18px;
  height: 2px;
  background: #9d80cb;
  margin: 3px 0;
  transition: 0.3s;
}

/* Animation de l'icône */
.active .burger span:nth-child(1) {
  transform: translateY(5px) rotate(45deg);
}
.active .burger span:nth-child(2) {
  transform: translateY(-5px) rotate(-45deg);
}

/* LE MENU DÉROULANT */
.dropdown {
  pointer-events: auto;
  clear: both; /* Se place sous le bouton */
  margin-top: 10px;
  background: white;
  padding: 15px;
  border-radius: 12px;
  border: 1px solid rgba(157, 128, 203, 0.1);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);

  /* Logique de taille pour ne jamais dépasser */
  width: max-content;
  max-width: calc(100vw - 40px); /* 100% de l'écran moins les marges */

  /* Animation d'apparition */
  opacity: 0;
  transform: translateY(-10px) scale(0.95);
  transition: all 0.3s ease;
  visibility: hidden;
}

.active .dropdown {
  opacity: 1;
  transform: translateY(0) scale(1);
  visibility: visible;
}

/* LIENS */
.dropdown a {
  display: block;
  text-decoration: none;
  color: #555;
  font-family: "Quicksand", sans-serif;
  font-size: 0.85rem;
  font-weight: 600;
  letter-spacing: 1px;
  padding: 10px 15px;
  white-space: nowrap;
}

.divider {
  height: 1px;
  background: rgba(157, 128, 203, 0.1);
  margin: 5px 15px;
}

/* Overlay invisible pour fermer */
.closer {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  z-index: -1;
  pointer-events: auto;
}

@media (max-width: 400px) {
  .menu-system {
    right: 10px; /* Plus serré sur petit mobile */
  }
}
</style>

<template>
  <img
    class="vuetify-logo"
    alt="Vuetify Logo"
    src="/vuetify-logo.svg"
  >
</template>

<style>
.vuetify-logo {
  height: 300px;
  width: 400px;
  transform: rotateY(560deg);
  animation: turn 4.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>

<template>
  <Homepage />
</template>

<script setup>
import Homepage from './views/Homepage.vue'
</script>


<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Exo:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,400&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Zen+Kaku+Gothic+Antique:wght@300;400;500;700;900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Electrolize&display=swap");
@import url("https://fonts.googleapis.com/css2?family=DM+Sans:ital,wght@0,400;0,500;0,700;1,400;1,500;1,700&display=swap");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
}

body {
  min-height: 100vh;
  background-color: $primary-color;
  font-family: "DM Sans", sans-serif !important;
  font-weight: 500;
  color: $font-color-secondary;
}

h2,
h3,
p,
a:not(.link-item) {
  font-family: "DM Sans", sans-serif;
}

@media screen and (max-width: 576px) {
  h2 {
    font-size: 1.8rem !important;
  }
}
</style>

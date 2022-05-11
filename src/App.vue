<template>
  <div class="header">
    <Navbar logo="Vuexp." />
    <HeroSection />
  </div>
</template>

<script>
import HeroSection from "./components/Hero.vue";
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  components: {
    HeroSection,
    Navbar,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  list-style-type: none;
  box-sizing: border-box;
}

.header {
  width: 100%;
  height: 90vh;
  background-color: #1d5af9;
}

.constrain {
  width: 100%;
  max-width: 90%;
  margin: 0 auto;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

@media (max-width: 768px) {
  .header {
    height: auto;
  }
}
</style>

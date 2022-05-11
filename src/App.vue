<template>
  <Navbar logo="Vuexp." />

  <div class="constrain">
    <div class="showcase">
      <img alt="Vue logo" src="./assets/logo.png" />
      <HelloWorld msg=" Blyncnov Welcome you to Vue 3 " />
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
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

.constrain {
  width: 100%;
  max-width: 90%;
  margin: 0 auto;
}

.showcase {
  margin: 1em 0;
  padding: 0 0.5em;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>

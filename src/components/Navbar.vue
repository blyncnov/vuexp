<template>
  <div class="navbar">
    <div class="constrain">
      <div class="navbar--logo">
        <h1>
          {{ logo }}
        </h1>
      </div>

      <ul @click="toggleNavbar" v-if="toggle" class="nav-list active">
        <li>Home</li>
        <li>About</li>
        <li>Experience</li>
        <li>Contact</li>
      </ul>

      <ul @click="toggleNavbar" v-else class="nav-list">
        <li>Home</li>
        <li>About</li>
        <li>Experience</li>
        <li>Contact</li>
      </ul>

      <div class="navbar--icon">
        <h1 @click="toggleNavbar">
          <h1 v-if="toggle">☰</h1>
          <h1 v-else>✕</h1>
        </h1>
      </div>
    </div>
  </div>
</template>
 
<script>
export default {
  name: "NavBar",
  props: {
    logo: String,
  },

  data() {
    return {
      toggle: true,
      text: "i hate you",
    };
  },

  methods: {
    toggleNavbar() {
      this.toggle = !this.toggle;
      console.log(this.toggle);
    },
  },
};
</script>
<style scoped>
.navbar {
  width: 100%;
  height: 80px;
  background-color: #fff;
  display: flex;
  align-items: center;
  padding: 0 1em;
  box-shadow: rgba(187, 191, 194, 0.2) 0px 8px 24px;
}

.constrain {
  width: 100%;
  max-width: 90%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar h1 {
  color: #3fb883;
  font-size: 30px;
  font-weight: 600;
}

ul,
li {
  display: flex;
  gap: 1em;
}

li {
  color: rgb(63, 184, 131, 0.9);
  font-weight: 500;
  cursor: pointer;
  font-size: 15px;
}

li:active {
  color: #3aa273;
}

.navbar--icon {
  display: none;
}

@media (max-width: 768px) {
  ul {
    display: block;
    width: 60%;
    height: 100vh;
    background-color: #3fb883;
    position: fixed;
    top: 0;
    left: 0;
    color: white !important;
    z-index: 999;
    transition: all 1s ease-in-out;
  }

  .active {
    left: -100%;
  }
  li {
    color: rgba(255, 255, 255);
    padding: 1em;
  }

  .navbar--icon {
    display: block;
  }
}
</style>
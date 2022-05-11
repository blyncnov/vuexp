<template>
  <div class="navbar">
    <div class="constrain">
      <ul
        @click="toggleNavbar"
        v-if="toggle"
        v-bind:class="toggle ? 'nav-list active' : 'nav-list'"
      >
        <li>Home</li>
        <li>About</li>
        <li>Testimonals</li>
        <li>Contact</li>
      </ul>

      <ul @click="toggleNavbar" v-else class="nav-list">
        <li>Home</li>
        <li>About</li>
        <li>Experience</li>
        <li>Contact</li>
      </ul>

      <div class="navbar--logo">
        <h1 class="logo">SmartHome</h1>
      </div>

      <div class="auth__method">
        <li>Login</li>
        <button class="signup__btn">Sign Up</button>
      </div>

      <div class="navbar--icon">
        <div @click="toggleNavbar">
          <h1 class="icon_hambuger" v-if="toggle">☰</h1>
          <h1 class="icon_hambuger" v-else>✕</h1>
        </div>
      </div>
    </div>
  </div>
</template>
 
<script scoped>
export default {
  name: "NavBar",
  props: {
    logo: String,
  },

  data() {
    return {
      toggle: true,
    };
  },

  methods: {
    toggleNavbar() {
      this.toggle = !this.toggle;
    },
  },
};
</script>
<style scoped>
.navbar {
  width: 100%;
  height: 80px;
  display: flex;
  align-items: center;
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
  color: #ffffff;
  font-size: 30px;
  font-weight: 600;
}

ul,
li {
  display: flex;
  gap: 1em;
}

li {
  color: #ffffff;
  font-weight: 600;
  cursor: pointer;
  font-size: 1.2rem;
}

li:active {
  color: rgb(232, 225, 225);
}

.auth__method {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2em;
}

.signup__btn {
  padding: 12px 24px;
  border-radius: 4px;
  color: black;
  background-color: #ffffff;
  font-weight: 600;
  font-size: 15px;
  outline: none;
  border: 1px solid #ffffff;
  cursor: pointer;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
}

.navbar--icon {
  display: none;
  cursor: pointer;
}

.navbar--icon div .icon_hambuger {
  color: #ffffff;
}

@media (max-width: 1000px) {
  .auth__method {
    display: none;
  }
}

@media (max-width: 768px) {
  ul {
    display: block;
    width: 60%;
    height: 100vh;
    background-color: #000000;
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
    padding: 0.5em 1em;
  }

  .navbar--icon {
    display: block;
  }
}
</style>
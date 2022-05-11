<template>
  <div class="hero__section--container">
    <div class="constrain">
      <div class="hero__text">
        <h1>Smart Home</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium
          commodi sapiente, autem dignissimos excepturi impedit culpa dolores,
          eius ea quibusdam amet natus modi aperiam? At cupiditate quas nemo
          beatae odit.
        </p>
      </div>
      <div class="hero__img">
        <img
          src="https://websitedemos.net/app-landing-page-04/wp-content/uploads/sites/600/2020/07/screenshot-004-free-img.png"
          alt="iphone"
        />
        <img
          src="https://websitedemos.net/app-landing-page-04/wp-content/uploads/sites/600/2020/07/screenshot-002-free-img.png"
          alt="iphone"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeroSection",

  data() {
    return {
      arr: [],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.constrain {
  width: 100%;
  max-width: 90%;
  margin: 0 auto;
}

.hero__section--container {
  text-align: center;
  color: white;
  padding: 2em 0;
}

.hero__section--container h1 {
  font-size: 4rem;
  font-weight: 900;
}

.hero__section--container p {
  font-size: 1.2rem;
  font-weight: 400;
  max-width: 60%;
  margin: 0 auto;
}

.hero__img {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2em;
  margin-top: 3em;
  margin-bottom: -30%;
}

.hero__img img {
  width: 20%;
  box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
  border-radius: 5px;
}

@media (max-width: 768px) {
  .hero__img {
    margin-bottom: -30%;
  }

  .hero__section--container h1 {
    font-size: 2.5rem;
  }

  .hero__section--container p {
    font-size: 13px;
    font-weight: 400;
    max-width: 100%;
    margin: 0 auto;
  }

  .hero__img img {
    width: 30%;
  }
}
</style>

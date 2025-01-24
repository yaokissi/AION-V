<template>
  <section class="page--content">
    <div class="left-side">
      <h2>Join us in reducing you carbon footprint, one charge at time.</h2>
      <p class="p--link--a--footprint pt-6 p-6">Learn More <a href="#">&rarr;</a> </p>
      <div class="social-media">
        <a href="#"><img src="../assets/img/linkedin.png" alt="facebook" height="40"></a>
        <a href="#"><img src="../assets/img/threads.png" alt="threads" height="40"></a>
        <a href="#"><img src="../assets/img/twitter.png" alt=" X (ex twitter)" height="40"></a>
      </div>
      <img src="../assets/img/aionV_calandre.jpg" width="100">
    </div>

    <div class="right-side">
      <div class="header">
        <nav>
          <img src="../assets/img/logoaionV.png" height="60">
          <ul>
            <li>Shop</li>
            <li>About Us </li>
            <li>Car Feature</li>
            <li>Electric Car</li>
          </ul>

          <button>Get in Touch</button>
        </nav>
        <div class="main">
          <h1>Drive the Future with Electric Cars</h1>
          <p>Discover the ultimate in efficiency and eco-friendliness. Our electric cars are designed to take you further with zero emissions.</p>
          <button>Learn More &rarr;</button>
        </div>
      </div>
      <div class="beling--show--learn--more">
        <h3>A Deep dive into the AION V.</h3>
        <p>At the 2024 Beling Auto Show, GAC unveiled the second generation AION V, a midsize SUV built on the AEP platform, <b>Learn More</b>  </p>
        <p>&#8600;</p>
      </div>
      <div class="stats--perf">
        <div v-for="stat in stats" :key="stat.label" class="text-center">
          <p class="">{{ stat.label }}</p>
          <h3 class="">{{ stat.value }}</h3>
        </div>
      </div>
      <div>
        <img src="../assets/img/AionVImage.jpg" width="250" height="150">
      </div>
    </div>
  </section>
</template>

<script>
import { ref } from "vue";

export default {
  name: "homeView",
  setup() {

    const stats = ref([
      { value: '100,000 Mah', label: 'Battery Capacity' },
      { value: '375+ Mph', label: 'Top Speed' },
      { value: '< 2kWh', label: 'Per km Energy' }
    ])
    return {
      stats
    };
  }
};
</script>

<style>


*{
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}
.page--content {
  display: flex;
  padding: 10px;
}
h2 {
  font-size: 1rem;
}
.left-side {
  width: 10%;
}
.right-side {
  width: 90%;
}
.p--link--a--footprint a {
  width: 100px; /* Largeur totale */
  padding: 3px;
  height: 200px; /* Hauteur = taille du cercle */
  border: 1px solid black;
  border-left: none;
  border-top-right-radius: 100px; /* Pas de rayon à droite */
  border-bottom-right-radius: 100px; /* Pas de rayon à droite */
}
.header {
  background-image: url("../assets/img/headerCover.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;
}
a {
  text-decoration: none;
  color: #000;
}
</style>

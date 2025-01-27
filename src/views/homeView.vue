<template>
  <section class="page--content">
    <div class="left-side">
      <img src="../assets/img/img.png">
      <h2>Join us in reducing you carbon footprint, one charge at time.</h2>
      <p class="p--link--a--footprint">Learn More <a href="#">&rarr;</a> </p>
      <div class="social-media">
        <a href="#"><img src="../assets/img/linkedin.png" alt="facebook" height="35"></a>
        <a href="#"><img src="../assets/img/threads.png" alt="threads" height="35"></a>
        <a href="#"><img src="../assets/img/twitter.png" alt=" X (ex twitter)" height="35"></a>
      </div>
      <div class="beling--show--learn--more">

        <img src="../assets/img/aionV_calandre.jpg" width="150">
        <h3>A Deep dive into the AION V.</h3>
        <p>At the 2024 Beling Auto Show, GAC unveiled the second <br> generation AION V, a midsize SUV built on the AEP <br> platform. <b>Learn More</b>  </p>
        <span class="down-arrow">&#8600;</span>
      </div>
    </div>

    <div class="right-side">
      <div class="header">
        <nav>
          <ul>
            <img src="../assets/img/logoaionV.png" height="60">
            <li>Shop</li>
            <li>About Us </li>
            <li>Car Feature</li>
            <li>Electric Car</li>
          </ul>

          <button>Get in Touch &rarr;</button>
        </nav>
        <div class="main">
          <h1>Drive the Future <br> with Electric Cars</h1>
          <p>Discover the ultimate in efficiency and eco- <br> friendliness. Our electric cars are designed to take <br> you further with zero emissions.</p>
          <button>Learn More &rarr;</button>
        </div>
      </div>

      <div class="stats--perf">
        <div class="aionv--characteristic">
          <div v-for="stat in stats" :key="stat.label" class="text-center">
            <p class="">{{ stat.label }}</p>
            <h3 class="">{{ stat.value }}</h3>
          </div>
        </div>
        <div class="aionv--video">
          <img src="../assets/img/AionVImage.jpg" width="250" height="200">
        </div>
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
      { value: '100.000 Mah', label: 'Battery Capacity' },
      { value: '375+ Mph', label: 'Top Speed' },
      { value: '< 2kWh', label: 'Per km Energy' }
    ])
    return {
      stats
    };
  }
};
</script>

<style lang="scss">


*{
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
}

.page--content {
  display: flex;
  padding: 10px;
  width: 95%;
  margin-left: auto;
  margin-right: auto;}
h2 {
  font-size: 1rem;
}
.left-side {
  width: 10%;
}
.right-side {
  width: 90%;
}
.p--link--a--footprint {
  margin-top: 30px;
  a {
    width: 100px;
    padding: 2px;
    height: 200px;
    border: 1px solid black;
    border-left: none;
    border-top-right-radius: 100px;
    border-bottom-right-radius: 100px;
  }
}
.social-media {
  margin-top: 400px;
  margin-bottom: 30px;
  a {
    display: block;
    margin-bottom: 10px;
  }
}

.beling--show--learn--more {

  padding: 7px 0 0 5px;
  width: 350px;
  height: 200px;
  background-color: #f4f4f4;
  position: relative;
  p {
    margin-top: 10px;
    font-size: 12px;
  }

  .down-arrow {
    display: inline-block;
    position: absolute;
    right: 5px;
    bottom: 5px;
    border: 2px solid black;
    border-radius: 50%;
    padding: 7px;
    text-align: center;
    line-height: 1;
    width: 10px;
    height: 10px;
  }
}


.header {
  background-image: url("../assets/img/headerCover.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  height: 100vh;

  /*
  &::before {
    content: "";
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.2); // Couleur noire avec 50% de transparence
    z-index: 1; // Place le calque au-dessus de l'image de fond
  } */
  .main{
    margin-left: 30px;
    p {
      font-size: 20px;
      margin-top: 10px;
      color: white;
    }
    button {
      padding: 20px;
      margin-top: 50px;
      background-color: #E65C01;
      color: white;
      width: 200px;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      font-size: 15px;
    }
  }
  h1 {
    font-size: 60px;
    margin-top: 70px;
    color: white;
  }
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
   /* background-color: rgba(0, 0, 0, 0.5); */
    color: white;
    img {
      margin-left: 10px;
    }
    ul {
      display: flex;
      list-style: none;
      align-items: center;
      li {
        margin-right: 20px;
        margin-left: 10px;
        cursor: pointer;
        background-color: rgba(0, 0, 0, 0.5);
        padding: 15px;
        border-radius: 50px;
      }
    }
    button {
      padding: 20px;
      background-color: black;
      color: white;
      width: 200px;
      border: none;
      border-radius: 50px;
      cursor: pointer;

    }
  }

}
a {
  text-decoration: none;
  color: #000;
}
.stats--perf {
  display: flex;
  justify-content: end;

  .aionv--video img{

    border-radius: 50px;
  }
}
.aionv--characteristic{

  width: 50%;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  p {
    font-size: 12px;
  }
  h3 {
    font-size: 35px;
    margin-top: 5px;
  }
}
</style>

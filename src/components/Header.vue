<template>
  <header>
    <!-- NAVBAR -->
    <nav>
      <div id="logo-container">
        <img src="../assets/construction_logo.png" alt="" />
      </div>
      <div id="nav-container">
        <ul>
          <li><a href="#">HOME</a></li>
          <li><a href="#">ABOUT</a></li>
          <li><a href="#">SERVICES</a></li>
          <li><a href="#">WORK</a></li>
          <li><a href="#">ARTICLES</a></li>
          <li>
            <button class="button-nav"><a href="#">GET QUOTE</a></button>
          </li>
        </ul>
      </div>
    </nav>
    <!-- JUMBOTRON -->
    <div class="jumbotron">
      <h2>BUILDING INSPIRING SPACES</h2>
      <span class="subtext"
        >We build Inspiring Residential &amp; Commercial Spaces</span
      >
      <div class="btn-container">
        <button class="button-work"><a href="#">EXPLORE RECENT WORK</a></button>
        <button class="button-quote"><a href="#">GET A QUOTE TODAY</a></button>
      </div>
    </div>
    <div class="yellow-container">
      <div id="yellow-title">
        Do You Have A Construction Project We Can Help With?
      </div>
    </div>
    <!-- MENU -->
    <div class="menu-container">
      <button class="btn-free-quote"><a href="#">GET A FREE QUOTE</a></button>
      <h4>Specialists In Modern Constructions</h4>
      <div class="line"></div>
      <p>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati
        ex quas, non veritatis provident soluta iure fuga, culpa molestias,
        debitis optio vel ipsa.
      </p>
      <!-- card -->
      <div class="construction-card">
        <ModernConstructionCard
          v-for="(service, i) in services"
          :key="i"
          :menu="service"
        />
      </div>
    </div>
  </header>
</template>

<script>
import ModernConstructionCard from "./ModernConstructionCard.vue";
export default {
  name: "Header",
  components: {
    ModernConstructionCard,
  },
  data() {
    return {
      services: [
        {
          class: "far fa-building",
          title: "Buildings",
          text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati provident soluta iure fuga, culpa ",
        },
        {
          class: "fas fa-sync",
          title: "Renovate",
          text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati provident soluta iure fuga, culpa ",
        },
        {
          class: "fas fa-home",
          title: "Construct",
          text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati provident soluta iure fuga, culpa ",
        },
        {
          class: "fas fa-truck",
          title: "Exclusive",
          text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eum obcaecati provident soluta iure fuga, culpa ",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
// NAVBAR
img {
  margin-top: 10px;
}
nav {
  display: flex;
  justify-content: space-between;
  width: 90%;
  margin-left: 5%;
  text-align: center;
  height: 115px;
}
ul {
  display: inline-block;
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  margin-top: 20px;
}

li {
  float: left;
  margin-top: 30px;

  a:hover {
    color: #fedc70;
  }
}

li a {
  display: block;
  padding: 8px;
  color: #858585;
  text-decoration: none;
  font-size: 19px;
}

.button-nav {
  background-color: #fed03d;
  color: #534c35;
  border: none;
  margin: 0 30px;

  a:hover {
    color: white;
  }
}
.button-nav:hover {
  background-color: #333333;
}

// JUMBOTRON

.jumbotron {
  background-image: url("../assets/home-slider-62528242.jpg");
  height: 805px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  flex-wrap: wrap;
}

.subtext {
  color: #f7ca3b;
  font-size: 25px;
}

h2 {
  color: white;
  display: block;
  font-size: 50px;
  margin: 15px;
}

.btn-container {
  margin-top: 30px;
}

.button-work {
  height: 55px;
  width: 300px;
  background-color: #333333;
  color: white;
  border: none;
  margin: 0 10px;

  a {
    display: block;
    padding: 8px;
    color: white;
    text-decoration: none;
    font-size: 19px;
  }

  a:hover {
    color: #f7ca3b;
  }
}
.button-quote {
  height: 55px;
  width: 300px;
  background-color: #fed03d;
  color: #534c35;
  border: none;
  margin: 0 10px;

  a {
    display: block;
    padding: 8px;
    color: #858585;
    text-decoration: none;
    font-size: 19px;
  }
}

.button-work:hover {
  background-color: #333333;
}

.button-quote:hover {
  background-color: #333333;
}

.yellow-container {
  background-color: #fed03d;
  height: 100px;
}

#yellow-title {
  font-size: 30px;
  padding-top: 30px;
}

// MENU

.btn-free-quote {
  background-color: #333333;
  border: 1px solid white;
  margin-top: -20px;

  a {
    color: white;
    display: block;
    padding: 8px;
    text-decoration: none;
    font-size: 19px;
  }
}

h4 {
  margin-top: 100px;
  margin-bottom: 30px;
  font-size: 35px;
}

p {
  font-size: 20px;
  width: 60%;
  margin-left: 20%;
}

.construction-card {
  margin-top: 60px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  width: 80%;
  margin-left: 10%;
}
.line {
  border: 1px solid #fed03d;
  margin: 40px 0px;
  width: 20%;
  margin-left: 40%;
}
</style>

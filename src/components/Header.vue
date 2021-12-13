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
      <span id="yellow-title"
        >Do You Have A Construction Project We Can Help With?</span
      >
    </div>
    <!-- MENU -->
    <div></div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
// NAVBAR
nav {
  display: flex;
  justify-content: space-between;
  width: 90%;
  margin-left: 5%;
  text-align: center;
  height: 135px;
}
ul {
  display: inline-block;
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
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
  margin-top: 30px;
}
</style>

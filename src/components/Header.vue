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
            <button><a href="#">GET QUOTE</a></button>
          </li>
        </ul>
      </div>
    </nav>
    <!-- JUMBOTRON -->
    <div></div>
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
header {
  width: 90%;
  margin-left: 5%;
  text-align: center;
}

// navbar
nav {
  display: flex;
  justify-content: space-between;
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
}

li a {
  display: block;
  padding: 8px;
  color: #858585;
  text-decoration: none;
  font-size: 19px;
}

a:hover {
  color: #fedc70;
}

button {
  background-color: #fed03d;
  color: #534c35;
  border: none;
  margin: 0 30px;

  a:hover {
    color: white;
  }
}

button:hover {
  background-color: #333333;
}
</style>

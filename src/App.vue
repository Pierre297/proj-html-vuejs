<template>
  <div id="app">
    <!-- HEADER -->
    <header>
      <Navbar />
      <Jumbotron />
      <Menu />
    </header>
    <!-- MAIN -->
    <main></main>
    <!-- FOOTER -->
    <footer></footer>
  </div>
</template>

<script>
// import header
import Navbar from "./components/Navbar.vue";
import Jumbotron from "./components/Jumbotron.vue";
import Menu from "./components/Menu.vue";
// import main
// import footer

export default {
  name: "App",
  components: {
    Navbar,
    Jumbotron,
    Menu,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

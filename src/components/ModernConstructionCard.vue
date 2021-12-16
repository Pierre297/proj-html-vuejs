<template>
  <div class="card">
    <div class="service-list">
      <div class="circle">
        <i :class="menu.class"></i>
      </div>
      <h3>{{ menu.title }}</h3>
      <p>{{ menu.text }}</p>
      <!-- card hover -->
      <div class="overlay text">
        <h3>ARTFULLY CRAFTED</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque ipsum
          fugiat maxime laudantium perferendis consequatur eligendi corrupt
        </p>
        <button><a href="#">GET A QUOTE</a></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModernConstructionCard",
  props: {
    menu: Object,
  },
};
</script>

<style scoped lang="scss">
.card {
  width: calc((100% / 4) - 40px);
  height: 375px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
.service-list {
  text-align: center;
  background-color: #f5f5f5;
  height: 300px;
  border-radius: 10px;
  position: relative;
}
.circle {
  border: 1px solid #747474;
  border-radius: 50%;
  width: 80px;
  height: 80px;
  margin-left: 38%;
  margin-top: 20px;
}

i {
  font-size: 35px;
  margin-top: 20px;
  color: #747474;
}

h3 {
  margin: 25px 0;
}

p {
  color: #a0a0a0;
}
// display testo hover
.overlay {
  position: absolute;

  bottom: 0;
  right: 0;
  height: 100%;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #fed03d;
}

.service-list:hover .overlay {
  opacity: 1;
  cursor: pointer;
}

.text {
  position: absolute;
  color: #1e1e1e;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;

  p {
    color: #1e1e1e;
    width: 80%;
    margin-left: 10%;
    margin-bottom: 20px;
  }
  h3 {
    padding-top: 30px;
    width: 80%;
    margin-left: 10%;
  }

  button {
    width: 140px;
    height: 50px;

    a {
      text-decoration: none;
    }
  }
}
</style>
<template>
  <footer>
    <!-- PARTNERS -->
    <div class="partner-container">
      <h3>Trusted Partners</h3>
      <div class="line"></div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi ut
        provident, incidunt ipsa quis dolorem quae vero, cumque reprehenderit
        expedita atque. Nisi error nobis ea voluptas eos ducimus, officiis
        culpa?
      </p>
      <Partnership
        v-for="(partner, i) in partners"
        :key="i"
        :partner="partner"
      />
    </div>
    <!-- FREE QUOTE -->
    <div class="free-quote-container">
      <div class="left-col">
        <h3>Building Inspiring Spaces</h3>
        <div class="secondline"></div>
        <p>
          quaerat suscipit, voluptatem beatae expedita numquam vitae corrupti
          labore aspernatur dolorem reprehenderit ullam?
        </p>
      </div>
      <div>
        <button><a href="#">GET A FREE QUOTE</a></button>
        <p class="buttontext">Only takes a few seconds!</p>
      </div>
    </div>
    <!-- CONTACT & INFO -->
    <div></div>
  </footer>
</template>

<script>
import Partnership from "./Partnership.vue";

export default {
  name: "Footer",
  components: {
    Partnership,
  },
  data() {
    return {
      partners: [
        {
          img: "home-logo11-219096700-320x202.png",
        },
        {
          img: "home-logo10-219096700-320x202.png",
        },
        {
          img: "home-logo2-219096700-320x202.png",
        },
        {
          img: "home-logo1-219096700-320x202.png",
        },
        {
          img: "home-logo9-219096700-320x202.png",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
// PARTNERS
.partner-container {
  margin-top: 30px;

  h3 {
    margin: 30px;
    font-size: 30px;
  }
  p {
    width: 40%;
    margin-left: 30%;
    line-height: 35px;
  }
}
.line {
  border: 1px solid #fed03d;
  margin: 60px 0px;
  width: 10%;
  margin-left: 45%;
}
// FREE QUOTE
.left-col {
  margin-left: 200px;
}
.free-quote-container {
  display: flex;
  justify-content: space-evenly;
  height: 350px;
  background-image: url("../assets/about-call-to-action-57862405.jpg");
  background-repeat: no-repeat;
  background-position: center center;

  text-align: start;

  h3 {
    color: white;
    font-size: 35px;
    margin-top: 100px;
    margin-right: 300px;
  }
  .secondline {
    border: 1px solid #fed03d;
    margin: 40px 0px;
    width: 40%;
    margin-left: 0;
  }
  p {
    color: white;
    font-size: 20px;
    width: 600px;
  }
  button {
    background-color: #fed03d;
    color: #534c35;
    border: none;
    width: 300px;
    height: 50px;
    margin: 150px 0 20px 40px;

    a {
      text-decoration: none;
      font-size: 20px;
    }
  }
  button:hover {
    background-color: #333333;
    cursor: pointer;
  }
  button:hover a {
    color: white;
  }
  .buttontext {
    margin-left: 40px;
  }
}
</style>
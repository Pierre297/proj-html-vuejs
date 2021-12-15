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
    <div></div>
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
</style>
<template>
  <main>
    <!-- STATISTICS -->
    <div class="statistics-container">
      <InfoCard v-for="(info, i) in infos" :key="i" :info="info" />
    </div>
    <!-- RECENT WORK -->
    <div></div>
    <!-- CORE VALUES -->
    <div></div>
    <!-- REVIEW -->
    <div></div>
    <!-- NEWS -->
    <div></div>
  </main>
</template>

<script>
import InfoCard from "./InfoCard.vue";

export default {
  name: "Main",
  components: {
    InfoCard,
  },
  data() {
    return {
      infos: [
        {
          thumb: "",
          number: "3534",
          role: "PLANNING APPLICATIONS",
        },
        {
          thumb: "",
          number: "896",
          role: "COMPLETED PROJECTS",
        },
        {
          thumb: "",
          number: "172",
          role: "TRAINED PROFESSIONALS",
        },
        {
          thumb: "",
          number: "19",
          role: "INTERNATIONALS OFFICES",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.statistics-container {
  margin-top: 60px;
  height: 550px;
  background-image: url("../assets/home-244125289.jpg");
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
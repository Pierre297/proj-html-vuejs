<template>
  <div>
    <div class="works-container">
      <img :src="require('../assets/' + work.image)" :alt="work.title" />
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentWork",
  props: {
    work: Object,
  },
};
</script>

<style scoped lang="scss">
.works-container {
  font-size: 20px;
  margin-top: 100px;
  width: 200px;

  img {
    width: 400px;
  }
}
</style>
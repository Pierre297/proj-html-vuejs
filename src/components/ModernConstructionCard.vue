<template>
  <div class="card">
    <div class="service-list">
      <img src="" alt="" />
      <h3>{{ menu.title }}</h3>
      <p>{{ menu.text }}</p>
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
}

h3 {
  margin: 25px 0;
}

p {
  color: #a0a0a0;
}
</style>
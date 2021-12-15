<template>
  <div class="card">
    <div class="service-list">
      <div class="circle">
        <i :class="menu.class"></i>
      </div>
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
</style>
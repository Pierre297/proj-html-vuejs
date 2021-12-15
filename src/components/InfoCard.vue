<template>
  <div class="info-card">
    <div class="">
      <i :class="info.class"></i>
      <h3>{{ info.number }}</h3>
      <p>{{ info.role }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "InfoCard",
  props: {
    info: Object,
  },
};
</script>

<style scoped lang="scss">
.info-card {
  margin: 40px;
  font-size: 20px;
  margin-top: 220px;
}
i {
  color: #fed03d;
  font-size: 60px;
}
h3 {
  color: #fed03d;
  font-size: 40px;
  margin: 20px;
}
p {
  color: white;
}
</style>
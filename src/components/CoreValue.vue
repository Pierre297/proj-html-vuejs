<template>
  <div class="card-value">
    <div>
      <h4>{{ value.title }}</h4>
      <div class="line"></div>
      <p>{{ value.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CoreValue",
  props: {
    value: Object,
  },
};
</script>

<style scoped lang="scss">
.card-value {
  margin: 40px;
  font-size: 20px;
  margin-top: 260px;
  width: 200px;
}
.line {
  border: solid 1px black;
  width: 10%;
  margin-left: 45%;
  margin: 20px auto;
}
</style>
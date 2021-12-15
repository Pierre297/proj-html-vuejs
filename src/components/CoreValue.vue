<template>
  <div class="card-value">
    <div>
      <div :class="value.color">
        <i :class="value.class"></i>
      </div>
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
  margin-top: 50px;
  width: 200px;
}
.line {
  border: solid 1px black;
  width: 10%;
  margin-left: 45%;
  margin: 20px auto;
}
i {
  color: white;
  font-size: 60px;
  padding-top: 20px;
}
// color icons
.lightblue {
  background-color: #4ea4a5;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  margin-left: 27%;
  margin-bottom: 25px;
}
.blue {
  background-color: #4e6da5;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  margin-left: 27%;
  margin-bottom: 25px;
}
.orange {
  background-color: #f6722a;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  margin-left: 27%;
  margin-bottom: 25px;
}
.green {
  background-color: #a7cf47;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  margin-left: 27%;
  margin-bottom: 25px;
}
</style>
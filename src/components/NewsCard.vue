<template>
  <div>
    <div class="news-card">
      <img :src="require('../assets/' + news.img)" alt="" />
      <span>{{ news.title }}</span>
      <p class="date">{{ news.date }}</p>
      <div class="line"></div>
      <p class="text">{{ news.text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewsCard",
  props: {
    news: Object,
  },
};
</script>

<style scoped lang="scss">
.news-card {
  margin: 0px 40px;
  margin-top: 80px;
  width: 300px;
  background-color: white;
  height: 500px;
}
.line {
  border: solid 1px #eae8e8;
  width: 80%;
  margin-left: 45%;
  margin: 20px auto;
}
.text {
  font-size: 15px;
  line-height: 30px;
}
.date {
  font-size: 12px;
  color: gray;
  margin-top: 15px;
}
img {
  width: 300px;
}
</style>
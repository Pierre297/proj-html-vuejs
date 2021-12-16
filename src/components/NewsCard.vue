<template>
  <div>
    <div class="news-card">
      <div class="card">
        <img :src="require('../assets/' + news.img)" alt="" />
        <span>{{ news.title }}</span>
        <p class="date">{{ news.date }}</p>
        <div class="line"></div>
        <p class="text-card">{{ news.text }}</p>
      </div>
      <div class="overlay text">
        <div class="icon">
          <div class="circle"><i class="fas fa-link"></i></div>
          <div class="circle"><i class="fas fa-search"></i></div>
        </div>
        <h4>Redeveloping Florida's Remote Southern Coast</h4>
        <p>Architecture, Buildings, Construction, News</p>
      </div>
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
  position: relative;
}
.line {
  border: solid 1px #eae8e8;
  width: 80%;
  margin-left: 45%;
  margin: 20px auto;
}
.text-card {
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

// display testo hover
.overlay {
  position: absolute;

  bottom: 0;
  right: 0;
  height: 37%;
  width: 100%;
  opacity: 0;
  transition: 0.5s ease;
  background-color: #fed03d;
}

.news-card:hover .overlay {
  opacity: 1;
  cursor: pointer;
}

.text {
  position: absolute;
  color: #1e1e1e;
  top: 18%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  text-align: center;

  p {
    color: #1e1e1e;
    width: 80%;
    margin-left: 10%;
    margin-bottom: 20px;
    color: white;
    font-size: 10px;
    margin-top: 5px;
  }
  h4 {
    padding-top: 45px;
    width: 80%;
    margin-left: 10%;
    color: white;
  }
}

.circle {
  background-color: white;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  display: inline-block;
  margin: 0 10px;
  margin-top: 30px;

  i {
    padding-top: 15px;
  }
}
</style>
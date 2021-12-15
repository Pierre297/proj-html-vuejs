<template>
  <div class="tweetcard">
    <img
      class="profilepic"
      :src="require('../assets/' + tweet.profilepic)"
      alt=""
    />
    <div class="name">
      <strong>{{ tweet.username }}</strong>
      <em>@{{ tweet.username }}</em>
    </div>
    <img class="logo" :src="require('../assets/' + tweet.logo)" alt="" />

    <p>{{ tweet.text }}</p>
    <img :src="require('../assets/' + tweet.img)" alt="" class="img-tweet" />
    <img :src="require('../assets/' + tweet.like)" alt="" class="like" />
    <img :src="require('../assets/' + tweet.share)" alt="" class="share" />
    <span class="data">{{ tweet.data }}</span>
  </div>
</template>

<script>
export default {
  name: "Twitter",
  props: {
    tweet: Object,
  },
};
</script>

<style scoped lang="scss">
.tweetcard {
  color: #6f6f6f;

  em {
    display: block;
  }
  p {
    margin-top: 20px;
  }
  .img-tweet {
    width: 400px;
    margin-top: 10px;
  }
  .profilepic {
    border-radius: 50%;
    width: 30px;
    margin: 0px 10px;
  }
  .logo {
    width: 30px;
    margin-left: 190px;
  }
  .name {
    display: inline-block;
  }
}
.data {
  margin-left: 290px;
  font-size: 15px;
}
</style>
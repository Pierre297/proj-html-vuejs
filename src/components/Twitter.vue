<template>
  <div class="tweetcard">
    <img
      class="profilepic"
      :src="require('../assets/' + tweet.profilepic)"
      alt=""
    />
    <strong>{{ tweet.username }}</strong>
    <img class="logo" src="" alt="" />
    <em>@{{ tweet.username }}</em>
    <p>{{ tweet.text }}</p>
    <img :src="require('../assets/' + tweet.img)" alt="" class="img-tweet" />
    <img src="" alt="" class="like" />
    <img src="" alt="" class="share" />
    <span>{{ tweet.data }}</span>
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
}
</style>
<template>
  <img :src="require('../assets/' + partner.img)" alt="" />
</template>

<script>
export default {
  name: "Partnership",
  props: {
    partner: Object,
  },
};
</script>

<style scoped lang="scss">
img {
  width: 200px;
  margin-top: 40px;
  margin-bottom: 40px;
}
</style>
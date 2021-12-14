<template>
  <div>
    <div class="">
      <img :src="work.image" :alt="work.title" />
    </div>
  </div>
</template>

<script>
export default {
  name: "RecentWork",
  props: {
    work: Object,
  },
};
</script>

<style scoped lang="scss">
</style>
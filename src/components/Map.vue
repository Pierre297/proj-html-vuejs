<template>
  <div>
    <GmapMap :center="center" :zoom="12" style="width: 100%; height: 400px" />
  </div>
</template>

<script>
export default {
  name: "Map",
  props: {
    map: Object,
  },
  data() {
    return {
      center: { lat: 51.50722, lng: -0.1275 },
    };
  },
};
</script>

<style scoped lang="scss">
</style>
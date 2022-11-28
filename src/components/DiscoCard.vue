<template>
  <div class="col">
    <div
      class="card"
      style="width: 18rem;"
    >
      <img
        :src="imgUrl"
        class="card-img-top"
        :alt="title"
      >
      <div class="card-body">
        <h2 class="title">
          {{ title }}
        </h2>
        <h4 class="artist">
          {{ artist }}
        </h4>
        <h4 class="year">
          {{ year }}
        </h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DiscoCard',
  props: {
    imgUrl: String,
    title: String,
    artist: String,
    year: String,
  },
};
</script>

<style lang="scss" scoped>

</style>

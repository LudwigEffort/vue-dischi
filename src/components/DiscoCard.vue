<template>
  <div class="col">
    <div
      class="card"
    >
      <img
        :src="imgUrl"
        class="card-img-top"
        :alt="title"
      >
      <div class="card-body">
        <h4 class="title">
          {{ title }}
        </h4>
        <p class="artist">
          {{ artist }}
        </p>
        <p class="year">
          {{ year }}
        </p>
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

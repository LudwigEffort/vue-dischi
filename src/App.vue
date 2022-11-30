<template>
  <div class="container">
    <HeaderPage />
    <MainPage />
  </div>
</template>

<script>
import HeaderPage from './components/HeaderPage.vue';
import MainPage from './components/MainPage.vue';

export default {
  nam: 'App',
  components: {
    HeaderPage,
    MainPage,
  },
};
</script>

<style lang="scss">
    @import "../node_modules/bootstrap/scss/bootstrap";
</style>

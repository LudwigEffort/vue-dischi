<template>
  <div class="container">
    <HeaderPage @change="onFiltersChange" />
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
  data() {
    return {
      selectedValue: 'none',
    };
  },
  methods: {
    onFiltersChange(newSelectedValue) {
      this.selectedValue = newSelectedValue;
    },
  },
};
</script>

<style lang="scss">
    @import "../node_modules/bootstrap/scss/bootstrap";
</style>

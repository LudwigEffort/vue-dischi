<template>
  <main class="container text-center p-4">
    <div
      v-if="arrDisco"
      class="row row-cols-4 g-5"
    >
      <DiscoCard
        v-for="disco in arrDisco"
        :key="disco.title"
        :img-url="disco.poster"
        :title="disco.title"
        :artist="disco.author"
        :year="disco.year"
      />
    </div>
    <div v-else>
      Loading...
    </div>
  </main>
</template>

<script>
import axios from 'axios';
import DiscoCard from './DiscoCard.vue';

export default {
  name: 'MainPage',
  components: {
    DiscoCard,
  },
  data() {
    return {
      arrDisco: null,
      urlAPI: 'https://flynn.boolean.careers/exercises/api/array/music',
    };
  },
  created() {
    axios.get(this.urlAPI)
      .then((axiosResponse) => {
        console.log(axiosResponse);
        this.arrDisco = axiosResponse.data.response;
      });
  },
};
</script>

<style lang="scss" scoped>
    main {
        background-color: #1E2D3B;
    }
</style>

<template>
  <div>
    <ul v-if="arrDisco">
      <li
        v-for="disco in arrDisco"
        :key="disco.title"
      >
        {{ disco.title }}
      </li>
    </ul>
    <div v-else>
      Loading...
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'MainPage',
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

<style>

</style>

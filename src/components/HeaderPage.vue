<template>
  <nav>
    <div class="container text-center p-2">
      <div class="row">
        <div class="col-1">
          <a
            class="navbar-brand"
            href="#"
          >
            <img
              src="../assets/spotify-logo.png"
              alt="Bootstrap"
              width="40"
              height="40"
            >
          </a>
        </div>
        <div class="col-3 offset-5">
          <select
            v-model="value"
            class="form-select"
            aria-label="Default select example"
            @change="$emit('change', value)"
          >
            <option value="none">
              Chose genre
            </option>
            <option value="Jazz">
              Jazz
            </option>
            <option value="Metal">
              Metal
            </option>
            <option value="Pop">
              Pop
            </option>
            <option value="Rock">
              Rock
            </option>
          </select>
        </div>
        <div class="col-3">
          <select
            class="form-select"
            aria-label="Default select example"
          >
            <option value="none">
              Chose author
            </option>
            <option value="Jazz">
              Jazz
            </option>
            <option value="Metal">
              Metal
            </option>
            <option value="Pop">
              Pop
            </option>
            <option value="Rock">
              Rock
            </option>
          </select>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'HeaderPage',
  data() {
    return {
      value: 'none',
    };
  },
};
</script>

<style lang="scss" scoped>
    nav {
        background-color: #2E3A46;
    }
</style>

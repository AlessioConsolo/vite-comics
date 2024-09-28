<template>
  <div class="card">
    <h2>{{ comic.series }}</h2>
  </div>
</template>
<script>
import dcComics from "../src/data/dc-comics.json";
export default {
  props: {
    comic: Object,
  },
  data() {
    return {
      comics: dcComics,
    };
  },
};
</script>
<style lang="scss">
.card {
  border: 1px solid #ddd;
  padding: 20px;
  margin: 20px;
  width: 200px;
}
</style>

<template lang="html">
  <div class="container">
    <div class="row">
      <div class="col">
        <div
          class="header-content d-flex gap-5 justify-content-between align-items-center mt-4"
        >
          <img src="../assets/dc-logo.png" alt="" />
          <ul class="list-unstyled d-flex mt-5">
            <li class="px-3" v-for="(link, index) in links" :key="index">
              <a class="" :href="link.url">
                <strong>{{ link.title }}</strong></a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      links: [
        { title: "CHARACTERS", url: "#" },
        { title: "COMICS", url: "#" },
        { title: "MOVIES", url: "#" },
        { title: "TV", url: "#" },
        { title: "GAMES", url: "#" },
        { title: "COLLECTIBLES", url: "#" },
        { title: "VIDEOS", url: "#" },
        { title: "FANS", url: "#" },
        { title: "NEWS", url: "#" },
        { title: "SHOP", url: "#" },
      ],
    };
  },
};
</script>
<style lang="scss">
a {
  text-decoration: none;
  color: black;
}

a:hover,
a:active {
  color: #2388f9;
}
</style>

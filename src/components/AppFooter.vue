<template lang="">
  <div class="top-footer container-fluid">
    <div class="container">
      <div class="row">
        <div class="col-2">
          <div class="contacts">
            <ul class="list-unstyled mt-5">
              <h5 class="text-white">DC COMICS</h5>
              <li v-for="(dcComic, index) in dcComics">
                <a :href="dcComic.url" class="text-secondary">{{
                  dcComic.title
                }}</a>
              </li>
            </ul>
            <ul class="list-unstyled my-5">
              <h5 class="text-white">SHOP</h5>
              <li v-for="(shop, index) in shops">
                <a :href="shop.url" class="text-secondary">{{ shop.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-2">
          <div class="contacts">
            <ul class="list-unstyled mt-5">
              <h5 class="text-white">DC</h5>
              <li v-for="(dc, index) in dcs">
                <a :href="dc.url" class="text-secondary">{{ dc.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-2">
          <div class="contacts">
            <ul class="list-unstyled mt-5">
              <h5 class="text-white">SITES</h5>
              <li v-for="(site, index) in sites">
                <a :href="site.url" class="text-secondary">{{ site.title }}</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-6"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dcComics: [
        { title: "Characters", url: "#" },
        { title: "Comics", url: "#" },
        { title: "Movies", url: "#" },
        { title: "TV", url: "#" },
        { title: "Games", url: "#" },
        { title: "Collectibles", url: "#" },
        { title: "Videos", url: "#" },
        { title: "Fans", url: "#" },
        { title: "News", url: "#" },
        { title: "Shop", url: "#" },
      ],
      shops: [
        { title: "Shop DC", url: "#" },
        { title: "Shop DC Collectibles", url: "#" },
      ],
      dcs: [
        { title: "Terms Of Use", url: "#" },
        { title: "Privacy Policy (New)", url: "#" },
        { title: "Ad Choices", url: "#" },
        { title: "Advertising", url: "#" },
        { title: "Jobs", url: "#" },
        { title: "Subscriptions", url: "#" },
        { title: "Talent Workshops", url: "#" },
        { title: "CPSC Certificates", url: "#" },
        { title: "Ratings", url: "#" },
        { title: "Shop Help", url: "#" },
        { title: "Contact Us", url: "#" },
      ],
      sites: [
        { title: "DC", url: "#" },
        { title: "MAD Magazine", url: "#" },
        { title: "DC Kids", url: "#" },
        { title: "DC Universe", url: "#" },
        { title: "DC Power Visa", url: "#" },
      ],
    };
  },
};
</script>
<style lang="scss">
.top-footer {
  background-image: url(/src/assets/dc-logo-bg.png),
    url(/src/assets/footer-bg.jpg);
  background-size: auto, cover;
  background-position: right;
  background-repeat: no-repeat, no-repeat;

  a {
    font-size: small;
  }
}
</style>

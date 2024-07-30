<template lang="">
  <div class="container-fluid bg-lightblack">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="cards my-5">
            <h2 class="text-white">-->Content goes here <--</h2>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="container-fluid bg-lightblue">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="middle-menu">
            <ul class="list-unstyled d-flex my-5 justify-content-between">
              <li v-for="(card, index) in middlecards">
                <img :src="getImageUrl(card.img)" alt="" class="px-2" />
                <a :href="card.url" class="text-white">{{ card.title }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      middlecards: [
        {
          img: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
          url: "#",
        },
        {
          img: "buy-comics-merchandise.png",
          title: "DC MERCHANDISE",
          url: "#",
        },
        {
          img: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
          url: "#",
        },
        {
          img: "buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR",
          url: "#",
        },
        {
          img: "buy-dc-power-visa.svg",
          title: "DC POWER VISA",
          url: "#",
        },
      ],
    };
  },
  methods: {
    getImageUrl(img) {
      return new URL(`../assets/${img}`, import.meta.url).href;
    },
  },
};
</script>
<style lang="scss">
.bg-lightblack {
  background-color: #1c1c1c;
}
.bg-lightblue {
  background-color: #0282f9;
}
.middle-menu img {
  height: 70px;
  width: auto;
}
</style>

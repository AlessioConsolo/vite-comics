<template>
  <div class="container-fluid jumbotron"></div>
  <div class="container-fluid bg-lightblack">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="title-text">
            <h4 class="text-white">CURRENT SERIES</h4>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col">
          <div class="cards">
            <Card v-for="comic in comics" :key="comic.id" :comic="comic" />
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
import Card from "./Cards.vue";
export default {
  components: { Card },
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
      comics: dcComics, // assegna il contenuto del file JSON a una variabile nel componente
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
.title-text {
  background-color: #0282f9;
  width: fit-content;
  padding: 10px;
  position: absolute;
  top: 525px;
}

.jumbotron {
  background-image: url("../assets/jumbotron.jpg");
  height: 400px;
  background-size: cover;
}

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

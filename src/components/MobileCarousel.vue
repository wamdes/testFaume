<template>
  <carousel :settings="settings">
    <slide v-for="slide in slides" :key="slide">
      <div class="carousel__item">
        <img :src="getImage(slide.img)" />
      </div>
    </slide>
    <template #addons>
      <navigation />
    </template>
  </carousel>
</template>
<script>
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Navigation } from "vue3-carousel";
export default {
  name: "MobileCarousel",
  data() {
    return {
      slides: [
        {
          img: "product1"
        },
        {
          img: "product2"
        },
        {
          img: "product3"
        },
        {
          img: "product4"
        }
      ]
    };
  },
  methods: {
    getImage(img) {
      return require("../assets/images/" + img + ".jpeg");
    }
  },
  components: {
    Carousel,
    Slide,
    Navigation
  },
  setup() {
    return {
      // carousel settings
      settings: {
        itemsToShow: 1,
        snapAlign: "center"
      }
    };
  }
};
</script>
<style lang="scss">
.carousel__item {
  max-height: 200px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    height: 200px;
  }
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
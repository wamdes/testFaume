<template>
  <section class="banner-large">
    <div class="banner-image">
      <img :src="require('../assets/images/femme.jpeg')" />
    </div>
    <div class="banner-text d-flex flex-column">
      <div class="text-center">FEMME</div>
      <div class="text-center">
        <button class="btn btn-outline-light">DECOUVRIR</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BannerLarge",
  components: {},
  mounted() {}
};
</script>

<style lang="scss">
.banner-large {
  .banner-text {
    font-weight: 700;
    font-size: 12vh;
    z-index: 2;
    position: relative;
    color: #fff;
    padding: 3em 0;
  }
  .banner-image {
    display: flex;
    justify-content: center;
    img {
      position: absolute;
      margin: auto;
    }
  }
}
</style>
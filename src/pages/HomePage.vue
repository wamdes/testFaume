<template>
  <div class="d-flex flex-column">
    <BannerLarge />
    <LargeText />
    <CollectionRow />
    <MobileCarousel v-if="isMobile()" />
    <ProductsRow v-else />
    <StoreRow />
  </div>
</template>

<script>
import BannerLarge from "@/components/BannerLarge";
import LargeText from "@/components/LargeText";
import CollectionRow from "@/components/CollectionRow";
import ProductsRow from "@/components/ProductsRow";
import StoreRow from "@/components/StoreRow";
import MobileCarousel from "@/components/MobileCarousel";

export default {
  name: "HomePage",
  methods: {
    getImage(img) {
      return require("../assets/images/" + img + ".jpeg");
    },
    isMobile() {
      if (screen.width <= 760) {
        return true;
      } else {
        return false;
      }
    }
  },

  components: {
    BannerLarge,
    LargeText,
    CollectionRow,
    ProductsRow,
    StoreRow,
    MobileCarousel
  }
};
</script>

<style lang="scss">
</style>
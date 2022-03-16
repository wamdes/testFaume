<template>
  <div class="logo col-4">
    <img :src="require('../assets/images/logo.svg')" />
  </div>
</template>

<script>
export default {
  name: "BrandLogo",
  mounted() {}
};
</script>

<style lang="scss">
.logo {
  text-align: center;
  img {
    height: 45%;
    z-index: 2;
    padding-top: 5px;
    filter: invert(1);
  }
}
</style>
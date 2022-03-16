<template>
  <li class="card">
    <div class="wrapper">
      <img
        :src="hovered === key ? getImage(product.img2) : getImage(product.img1)"
        @mouseover="hovered = key"
        @mouseleave="hovered = null"
      />
    </div>
    <div class="name">{{product.name}}</div>
    <div class="price">{{product.price}} £</div>
  </li>
</template>
<script>
export default {
  name: "ProductCard",
  props: ["product"],
  data() {
    return {
      hovered: null
    };
  },
  methods: {
    getImage(img) {
      return require("../assets/images/" + img + ".jpeg");
    }
  },
  mounted() {}
};
</script>
<style lang="scss">
.card {
  border: none;
  .wrapper {
    display: inline-flex;
    margin: 0 7px;
    img:hover {
      opacity: 0.5;
    }
  }
  .name {
    font-weight: 700;
  }
}
</style>
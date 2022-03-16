<template>
  <li class="card">
    <div class="wrapper">
      <img :src="getImage(item.img)" />
    </div>
    <div class="title">{{item.title}}</div>
  </li>
</template>
<script>
export default {
  name: "CardHalfScreen",
  props: ["item"],
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
  width: 49%;

  .wrapper {
    height: 100%;
    overflow: hidden;
    display: inline-flex;

    img {
      width: 100%;
    }
  }
  .title {
    color: #fff;
    font-weight: 700;
    position: absolute;
    bottom: 2em;
    padding-left: 2em;
  }
}
</style>
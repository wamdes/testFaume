<template>
  <Popper content="Aucun article dans le panier">
    <div class="cart-icon col-4">
      <button>
        <img :src="require('../assets/images/icon-cart.png')" />
      </button>
    </div>
  </Popper>
</template>

<script>
import Popper from "vue3-popper";
export default {
  name: "CartIcon",
  components: {
    Popper
  },
  mounted() {}
};
</script>

<style lang="scss">
:root {
  --popper-theme-background-color: #fff;
  --popper-theme-text-color: #000;
  --popper-theme-border-width: 0px;
  --popper-theme-border-style: solid;
  --popper-theme-border-radius: 6px;
  --popper-theme-padding: 32px;
  --popper-theme-box-shadow: 0 6px 30px -6px rgba(0, 0, 0, 0.25);
}
.cart-icon {
  button {
    filter: invert(1);
    height: 2em;
    text-align: right;

    img {
      height: 100%;
    }
  }
}
</style>
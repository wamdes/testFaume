<template>
  <div>
    <header class="d-inline-flex justify-content-between">
      <MainMenu />
      <BrandLogo />
      <CartIcon />
    </header>
    <main>
      <slot />
    </main>
    <footer>
      <FooterMenu />
    </footer>
  </div>
</template>

<script>
import MainMenu from "@/components/MainMenu";
import BrandLogo from "@/components/BrandLogo";
import CartIcon from "@/components/CartIcon";
import FooterMenu from "@/components/FooterMenu";

export default {
  name: "DefaultLayout",
  components: { MainMenu, BrandLogo, CartIcon, FooterMenu },
  mounted() {
    let w_out_sticky = document.querySelector("header");

    window.addEventListener("scroll", () => {
      window.scrollY > 300
        ? w_out_sticky.classList.add("sticky")
        : w_out_sticky.classList.remove("sticky");
    });
  }
};
</script>

<style lang="scss">
.sticky {
  background-color: #fff;
  .cart-icon {
    filter: invert(0);
  }
  .navbar {
    display: inline-block;
    .nav {
      .item {
        color: #000;
      }
    }
  }
  .logo {
    img {
      filter: invert(0%);
    }
  }
}
</style>
<template>
  <div class="container footer-menu">
    <ul class="d-flex">
      <li v-for="link in links" :key="link.index">
        <a :href="link.url">{{link.label}}</a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "FooterMenu",
  data() {
    return {
      links: [
        { label: "Faq", url: "faq" },
        { label: "Mentions légales", url: "#" },
        { label: "CGV", url: "#" }
      ]
    };
  }
};
</script>
<style lang="scss">
.footer-menu {
  width: 100%;
  ul {
    position: relative;
    justify-content: center;
    li {
      margin: 5% 5%;
      display: inline-block;
      white-space: nowrap;
      a {
        text-decoration: none;
        font-weight: 700;
        color: #fff;
      }
    }
  }
}
</style>
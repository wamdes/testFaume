<template>
  <nav class="navbar col-4">
    <ul class="nav">
      <li class="item col-4">HOMME</li>
      <li class="item col-4">FEMME</li>
      <li class="item col-4">CONCEPT</li>
    </ul>
  </nav>
</template>


<script>
export default {
  name: "MainMenu",
  mounted() {}
};
</script>

<style lang="scss">
.navbar {
  align-items: unset !important;
  .nav {
    padding: 0.5em;

    .item {
      font-weight: 700;
    }
  }
}
</style>

<template>
  <div class="large-text text-center d-flex flex-column">
    <h1>Lorem ipsum dolor sit amet</h1>
    <div class="content">
      Et pariatur iusto et atque dolorum aut voluptatum fuga ab reprehenderit voluptatem est recusandae architecto.
      Et placeat quia qui necessitatibus laborum aut quas nulla id omnis eveniet et quaerat recusandae vel ipsam atque.
      Et ullam libero et corrupti repellat ea iusto enim et fugiat enim ab iste voluptate sed velit possimus ea recusandae
      consequuntur? Aut voluptates perspiciatis sed voluptas odio reiciendis alias aut omnis commodi id dolore tempore nam illum facere.
    </div>
    <div class="text-center">
      <button class="btn btn-outline-dark">DECOUVRIR</button>
    </div>
  </div>
</template>
<script>
export default {
  name: "LargeText",
  mounted() {}
};
</script>
<style lang="scss">
.large-text {
  position: relative;
  width: 100%;
  margin: 0 auto;
  padding: 10em 0.5em;
  font-weight: 400;

  h1 {
    text-transform: uppercase;
    line-height: 1em;
  }
  .content {
    margin-bottom: 7%;
  }
}
</style>
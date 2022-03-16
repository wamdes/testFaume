<template>
  <section class="store">
    <ul class="d-flex flex-row">
      <CardHalfScreen v-for="item in items" :key="item.index" :item="item" />
      <li class="card">
        <div class="text-center no-image">
          <button class="btn btn-outline-dark align-middle">DECOUVRIR</button>
        </div>
      </li>
    </ul>
  </section>
</template>
<script>
import CardHalfScreen from "@/components/CardHalfScreen";
export default {
  name: "StoreRaw",
  components: { CardHalfScreen },
  data() {
    return {
      items: [
        {
          title: "",
          img: "store"
        }
      ]
    };
  },
  methods: {
    getImage(img) {
      return require("../assets/images/" + img + ".jpeg");
    }
  }
};
</script>
<style lang="scss">
.store {
  margin-top: 2em;

  ul {
    display: flex;
    flex-wrap: wrap;
  }
  .no-image {
    height: 100%;
    background-color: #eee;
    padding-top: 28%;
  }
}
</style>
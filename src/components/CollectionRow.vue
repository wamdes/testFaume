<template>
  <section class="collection-row">
    <ul class="d-flex flex-row">
      <CardHalfScreen v-for="item in items" :key="item.index" :item="item" />
    </ul>
  </section>
</template>
<script>
import CardHalfScreen from "@/components/CardHalfScreen";
export default {
  name: "CollectionRaw",
  components: { CardHalfScreen },
  data() {
    return {
      items: [
        {
          title: "COLLECTION FEMME",
          img: "robe"
        },
        { title: "COLLECTION HOMME", img: "homme" }
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
.collection-row {
  margin-top: 2em;
  ul {
    display: flex;
    flex-wrap: wrap;
  }
}
</style>
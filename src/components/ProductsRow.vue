<template>
  <section class="products-row">
    <h2>NOTRE SELECTION</h2>
    <ul class="d-flex flex-row">
      <ProductCard v-for="product in products" :key="product.index" :product="product" />
    </ul>
  </section>
</template>
<script>
import ProductCard from "@/components/ProductCard";
export default {
  name: "ProductsRow",
  components: { ProductCard },
  data() {
    return {
      products: [
        {
          name: "T-shirt Homme",
          img1: "product1",
          img2: "product7",
          price: "70.00"
        },
        {
          name: "veste cuir",
          img1: "product2",
          img2: "product7",
          price: "170.00"
        },
        {
          name: "Trench Homme",
          img1: "product3",
          img2: "product6",
          price: "250.00"
        },
        {
          name: "Sac cuir",
          img1: "product4",
          img2: "product5",
          price: "360.00"
        }
      ]
    };
  },
  mounted() {}
};
</script>
<style lang="scss">
h2 {
  margin-left: 1em;
}
</style>
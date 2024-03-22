<!-- MAIN -->
<script>
import Card from "./Card.vue";
import products from "./db.json";
export default {
  components: {
    Card,
  },
  data() {
    return {
      productsList: products,
    };
  },
  mounted() {
    console.log(this.productsList);
  },
};
</script>

<template>
  <div class="wrapper">
    <!-- bel trick quello di mettere l' array nell' oggetto, ci ho perso giusto un ora hahah -->
    <Card
      v-for="product in productsList.products"
      :key="product.id"
      :product="product"
    />
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  padding-top: 60px;

  .container {
    text-align: center;
    display: flex;
    flex-wrap: wrap;
  }
}
</style>

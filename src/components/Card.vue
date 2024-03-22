<script>
import products from "./db.json";
export default {
  data() {
    return {
      products: products.products,
      newProducts: [],
    };
  },
  computed() {},
  mounted() {
    this.newProducts = this.products.map((product) => ({
      ...product,
      badges: [
        ...product.badges,
        {
          type: "",
          value: "",
        },
      ],
    }));
    console.log(this.newProducts);
  },
};
</script>

<template>
  <div
    class="card-wrapper"
    v-for="(product, index) in newProducts"
    :key="index"
  >
    <div class="card-image">
      <img :src="`src/assets/img/${product.frontImage}`" alt="" />
    </div>
    <div class="tag">
      <div
        class="badge"
        :class="{
          sost: product.badges[0].value === 'Sostenibilità',
          discount: product.badges[0].value !== 'Sostenibilità',
        }"
      >
        {{ product.badges[0].value }}
      </div>
      <div
        class="badge"
        :class="{
          discount: product.badges[1].value !== 'Sostenibilità',
          '': product.badges[1].value !== '',
        }"
      >
        {{ product.badges[1].value }}
      </div>
    </div>
    <div class="liked">
      <div>
        <span><i class="fa-solid fa-heart"></i></span>
      </div>
    </div>
    <div class="info"></div>
  </div>
</template>

<style lang="scss" scoped>
@import "../../src/assets/scss/main.scss";
.card-wrapper {
  width: calc(80% / 3);
  height: 600px;
  max-width: 460px;
  margin: 20px 5px 40px;
  position: relative;
  background-color: rgba(255, 193, 77, 0.433);
  .card-image {
    width: 100%;
    background-color: rgba(255, 0, 0, 0.288);
  }
  .tag {
    position: absolute;
    top: 65%;
    z-index: 3;
    background-color: rgba(128, 0, 128, 0.363);
    height: 7%;
    width: 100%;
    display: flex;
    .badge {
      margin: 10px 5px;
    }
  }
  .liked {
    height: 50px;
    width: 40px;
    background-color: orange;
    position: absolute;
    top: 20px;
    right: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .info {
    height: 20%;
    width: 100%;
    background-color: rgba(0, 128, 0, 0.401);
  }
}
.discount {
  background-color: red;
}
.sost {
  background-color: green;
}
</style>

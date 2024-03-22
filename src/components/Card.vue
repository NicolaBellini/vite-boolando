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
      <img
        :src="`src/assets/img/${product.backImage}`"
        alt=""
        class="hovered-image"
      />
    </div>
    <div class="tag">
      <!-- applico la classe sostenibilità solo se il .value è uguale a sostenibilità -->
      <div
        class="badge"
        :class="{
          sost: product.badges[0].value === 'Sostenibilità',
          discount: product.badges[0].value !== 'Sostenibilità',
        }"
      >
        {{ product.badges[0].value }}
      </div>
      <!-- applico la classe discount o una stringa vuota se il value è diverso da sostenibilità o striga vuota -->
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
    <div class="liked" @click="product.isInFavorites = !product.isInFavorites">
      <div>
        <span
          ><i
            class="fa-solid fa-heart"
            :class="{ favorite: product.isInFavorites }"
          ></i
        ></span>
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
    position: relative;
    width: 100%;
    background-color: rgba(255, 0, 0, 0.288);
    &:hover .hovered-image {
      display: block;
    }
    .hovered-image {
      position: absolute;
      top: 0;
      display: none;
    }
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
      color: rgb(255, 255, 255);
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 10px 5px;
    }
  }
  .liked {
    height: 50px;
    width: 40px;
    background-color: rgb(255, 255, 255);
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
.favorite {
  color: red;
}
</style>

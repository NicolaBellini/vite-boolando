<script>
export default {
  props: {
    product: Object,
  },
  mounted() {
    console.log(this.product);
  },
};
</script>

<template>
  <div class="card-wrapper">
    <div class="card-image">
      <!-- <img src="`../../src/assets/img/${product.backImage}`" alt="" /> -->
    </div>
    <div class="tag"></div>
    <div class="liked">
      <div>
        <span><i class="fa-solid fa-heart"></i></span>
      </div>
    </div>
    <div class="info">{{ product.name }}</div>
  </div>
</template>

<style lang="scss" scoped>
@import "../../src/assets/scss/main.scss";
.card-wrapper {
  width: calc(80% / 3);
  height: 600px;
  max-width: 460px;
  margin: 20px 5px 180px;
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
</style>

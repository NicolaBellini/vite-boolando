<!-- MAIN -->
<script>
import Card from "./Card.vue";

export default {
  components: {
    Card,
  },
};
</script>

<template>
  <div class="wrapper">
    <!-- bel trick quello di mettere l' array nell' oggetto, ci ho perso giusto un ora hahah -->
    <div class="container">
      <Card />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  padding-top: 60px;
  display: flex;

  .container {
    margin: 0 auto;
    text-align: center;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
  }
}
</style>

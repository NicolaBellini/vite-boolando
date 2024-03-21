<!-- HEADER -->
<script>
export default {};
</script>

<template>
  <div class="wrapper debug">
    <div class="container debug">
      <div class="left">l</div>
      <div class="center">c</div>
      <div class="rigth">r</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/variables" as *;

.wrapper {
  height: 60px;
  display: flex;
  justify-content: center;
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}
</style>

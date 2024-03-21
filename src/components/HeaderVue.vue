<!-- HEADER -->
<script>
export default {};
</script>

<template>
  <div class="wrapper debug">
    <div class="container debug">
      <div class="left">l</div>
      <div class="center">
        <img src="../assets/img/boolean-logo.png" alt="" />
      </div>
      <div class="rigth">r</div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/variables" as *;

.wrapper {
  color: $header-words;
  background-color: $header-bg;
  height: 60px;
  display: flex;
  justify-content: center;
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    .left {
      width: 40%;
    }
    .center {
      width: 15%;
    }
    .rigth {
      width: 40%;
      display: flex;
      justify-content: flex-end;
    }
  }
}
</style>

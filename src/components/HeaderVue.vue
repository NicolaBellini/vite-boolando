<!-- HEADER -->
<script>
export default {
  // data() {
  //   return {
  //     logo:'boolean-logo.png',
  //   }
  // },
  // methods: {
  //   getImage(img){
  //     return
  //   }
  // },
};
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="left">
        <div class="donna"><span>Donna</span></div>
        <div class="uomo"><span>Uomo</span></div>
        <div class="bambini"><span>Bambini</span></div>
      </div>
      <div class="center">
        <img src="../assets/img/boolean-logo.png" alt="" />
      </div>
      <div class="rigth">
        <i class="fa-regular fa-user"></i>
        <i class="fa-regular fa-heart"></i>
        <i class="fa-solid fa-bag-shopping"></i>
      </div>
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
      display: flex;
      span {
        cursor: pointer;
        font-size: 1.2rem;
        margin-right: 20px;
        &:hover {
          color: darken($header-words, 60%);
        }
      }
    }
    .center {
      width: 15%;
    }
    .rigth {
      width: 40%;
      display: flex;
      justify-content: flex-end;
      i {
        cursor: pointer;
        font-size: 1.2rem;
        margin-left: 10px;
        &:hover {
          color: darken($header-words, 60%);
        }
      }
    }
  }
}
</style>

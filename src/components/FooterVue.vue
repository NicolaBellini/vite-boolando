<!-- FOOTER -->
<script>
export default {};
</script>

<template>
  <div class="wrapper">
    <div class="container">
      <div class="col-left">
        <h4>Booleando s.r.l.</h4>
        <ul>
          <li>Informazioni legali</li>
          <li>Informativa sulla privacy</li>
          <li>Diritto di recesso</li>
        </ul>
      </div>
      <div class="col-rigth">
        <h4>Trovaci anche su</h4>
        <div class="social-icon">
          <!-- icome social -->
          <i class="fa-brands fa-square-facebook"></i>
          <i class="fa-brands fa-square-x-twitter"></i>
          <i class="fa-brands fa-square-instagram"></i>
          <i class="fa-brands fa-square-pinterest"></i>
          <i class="fa-brands fa-square-youtube"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../assets/scss/variables" as *;
.wrapper {
  color: $footer-words;
  background-color: $footer-bg;
  height: 100px;
  .container {
    display: flex;
    justify-content: space-between;
    .col-left {
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 20px;
      width: 70%;
      h4 {
        cursor: pointer;
        &:hover {
          color: darken($footer-words, 60%);
        }
      }
      ul {
        margin-top: 20px;
        display: flex;
        list-style: none;
        li {
          margin-right: 10px;
          cursor: pointer;
          &:hover {
            color: darken($footer-words, 60%);
          }
        }
      }
    }
    .col-rigth {
      width: 30%;
      display: flex;
      align-items: flex-end;
      justify-content: center;
      flex-direction: column;
      padding: 20px;
      h4:hover {
        cursor: pointer;
        color: darken($footer-words, 60%);
      }
      .social-icon i {
        margin-top: 20px;
        margin-right: 5px;
        cursor: pointer;
        &:hover {
          color: darken($footer-words, 60%);
        }
      }
    }
  }
}
</style>

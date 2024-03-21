<!-- FOOTER -->
<script>
export default {};
</script>

<template>
  <div class="wrapper">
    <div class="container debug">
      <div class="col-left debug">
        <h4>Booleando s.r.l.</h4>
        <ul>
          <li>Informazioni legali</li>
          <li>Informativa sulla privacy</li>
          <li>Diritto di recesso</li>
        </ul>
      </div>
      <div class="col-rigth debug"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
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
      ul {
        margin-top: 20px;
        display: flex;
        list-style: none;
        li {
          margin-right: 10px;
        }
      }
    }
    .col-rigth {
      width: 30%;
      display: flex;
      justify-content: flex-end;
    }
  }
}
</style>

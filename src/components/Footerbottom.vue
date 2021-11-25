<template>
  <div class="footer-bottom">
    <div class="container">
      <div class="sign-up">
        <a href="">sign-up now!</a>
      </div>
      <div class="follow">
        <a href="">follow us</a>
        <a href="">
          <img src="../assets/img/footer-facebook.png" alt="">
        </a>
        <a href="">
          <img src="../assets/img/footer-twitter.png" alt="">
        </a>
        <a href="">
          <img src="../assets/img/footer-youtube.png" alt="">
        </a>
        <a href="">
          <img src="../assets/img/footer-pinterest.png" alt="">
        </a>
        <a href="">
          <img src="../assets/img/footer-periscope.png" alt="">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
   name: 'Footerbottom',

}
</script>

<style lang="scss">

@import "../assets/style/vars.scss";
@import "../assets/style/mixin.scss";

.footer-bottom{
  height: 130px;
  background-color: $primary-color;
  .container{
    @include between();
    height: 100%;
    .sign-up{
      a{
        color: white;
        text-transform: uppercase;
        text-decoration: none;
        height: 35px;
        border: 2px solid $merchandaise-color;
        padding: 12px 15px;
        transition: 0.4s;
        &:hover{
          border: 2px solid white;
          color: white;
          background-color: rgba(255, 255, 255, 0.445)
        }
      }
    }
    .follow{
      @include center();
      a{
        @include center();
        color: $logo-color;
        text-transform: uppercase;
        text-decoration: none;
        height: 35px;
        font-weight: bold;
        margin-left: 20px;
        transition: 0.2s;
        &:hover{
          filter: invert(1);
        }
      }
    }
  }
}
</style>
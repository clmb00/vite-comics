<script>

export default{
  name: 'FooterSocialApp',
}

</script>

<template>
  <div id="social-bar">
    <div class="container">
      <button>Sign-up Now!</button>
      <div class="social">
        <a href="#">Follow Us</a>
        <div class="btn">
          <a href="#"><img src="../assets/img/footer-facebook.png" alt=""></a>
        </div>
        <div class="btn">
          <a href="#"><img src="../assets/img/footer-twitter.png" alt=""></a>
        </div>
        <div class="btn">
          <a href="#"><img src="../assets/img/footer-youtube.png" alt=""></a>
        </div>
        <div class="btn">
          <a href="#"><img src="../assets/img/footer-pinterest.png" alt=""></a>
        </div>
        <div class="btn">
          <a href="#"><img src="../assets/img/footer-periscope.png" alt=""></a>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

#social-bar{
  height: $footer-social-height;
  background-color: $l-black;
  .container{
    @include flex('vertical');
    justify-content: space-between;
    button{
      cursor: pointer;
      padding: 12px;
      border: 2px solid $blue;
      color: white;
      background-color: $background-button;
      text-transform: uppercase;
      position: relative;
      z-index: 1;
      transition: color .5s ease-in-out;
      &:hover{
        color: $blue;
      }
      &::before{
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: white;
        z-index: -1;
        transform: scaleX(0);
        transform-origin: left;
        transition: transform .4s ease-in-out;
      }
      &:hover::before{
        transform: scaleX(1);
      }
    }
    .social{
      @include flex;
      a{
        color: $blue;
        text-transform: uppercase;
        font-weight: bold;
        margin-right: 20px;
        line-height: $footer-social-height;
        img{
          vertical-align: middle;
          &:hover{
            filter: brightness(2);
          }
        }
      }
    }
  }
}


</style>
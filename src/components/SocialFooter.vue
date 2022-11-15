<script>

export default{
  name: 'SocialFooter',
}

</script>

<template>
  <div id="social-bar">
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
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

#social-bar{
  height: 110px;
  @include flex('vertical');
  justify-content: space-between;
  button{
    padding: 10px;
    border: 2px solid $blue;
    color: white;
    background-color: transparent;
    text-transform: uppercase;
    cursor: pointer;
    &:hover{
      transform: scale(1.05)
    }
  }
  .social{
    @include flex;
    a{
      color: $blue;
      text-transform: uppercase;
      margin-right: 20px;
      line-height: 110px;
      img{
        vertical-align: middle;
        &:hover{
          filter: brightness(2);
        }
      }
    }
  }
}


</style>
<script>

export default{
  name: 'BlueSectionApp',
  data(){
    return{
      buyComics: [
        {
          name: 'Digital Comics',
          src: 'buy-comics-digital-comics.png'
        }, {
          name: 'Dc Merchandise',
          src: 'buy-comics-merchandise.png'
        }, {
          name: 'Subscription',
          src: 'buy-comics-subscriptions.png'
        }, {
          name: 'Comics Shop Locator',
          src: 'buy-comics-shop-locator.png'
        }, {
          name: 'Dc Power Visa',
          src: 'buy-dc-power-visa.svg'
        }
      ]
    }
  },
  methods:{
    getPathImage(imageName){
      return new URL(`../assets/img/${imageName}`, import.meta.url).href
    }
  }
}

</script>

<template>
  <section>
    <div class="container">
      <div v-for="(item, index) in buyComics" :key="index">
        <div class="logo">
          <img :src="getPathImage(item.src)" :alt="item.name">
        </div>
        <span>{{item.name.toUpperCase()}}</span>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

section{
  background-color: $blue;
  color: white;
  .container{
    height: 155px;
    @include flex('vertical');
    flex-wrap: wrap;
    justify-content: space-evenly;
  }
  div{
    @include flex('both');
    .logo{
      width: 50px;
      margin-right: 10px;
      img{
        height: 50px;
      }
    }
    span{
      font-size: .8rem;
      white-space: nowrap;
    }
  }
}
</style>
<script>

export default{
  name: 'HeaderApp',
  data(){
    return{
      currentPage: 'Comics',
      menuVoices: [
      {
        pageName: 'Characters',
        href: '#',
        current: false //useless for now
      }, {
        pageName: 'Comics',
        href: '#',
        current: false
      }, {
        pageName: 'Movies',
        href: '#',
        current: false
      }, {
        pageName: 'Tv',
        href: '#',
        current: false
      }, {
        pageName: 'Games',
        href: '#',
        current: false
      }, {
        pageName: 'Collectibles',
        href: '#',
        current: false
      }, {
        pageName: 'Videos',
        href: '#',
        current: false
      }, {
        pageName: 'Fans',
        href: '#',
        current: false
      }, {
        pageName: 'News',
        href: '#',
        current: false
      }, {
        pageName: 'Shop',
        href: '#',
        current: false
      }
      ]
    }
  }
}

</script>

<template>
  <header>
    <div class="container">
      <div class="logo">
        <img src="/dc-logo.png" alt="DC Logo">
      </div>
      <nav>
        <ul>
          <li v-for="(item, index) in menuVoices" :key="index" :class="{'active' : (item.pageName == currentPage)}"><a :href="item.href" @click="currentPage = item.pageName">{{item.pageName.toUpperCase()}}</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

header{
  height: $footer-height;
  background-color: #fff;
}

.container{
  @include flex('vertical');
  justify-content: space-between;
}

.logo{
  width: 80px;
}

ul{
  height: $footer-height;
}

li{
  height: 100%;
  line-height: 120px;
  text-align: center;
  min-width: 30px;
  display: inline-block;
  margin-left: 30px;
  &.active{
      color: $blue;
      border-bottom: 5px solid $blue;
      a{
        color: $blue;
      }
    }
  a{
    font-size: .85rem;
    color: $black;
    &:hover{
      color: $blue;
    }
  }
}

</style>
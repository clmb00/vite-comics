<script>

export default{
  name: 'HeaderApp',
  data(){
    return{
      menuVoices: [
      {
        pageName: 'Characters',
        href: '#',
        current: false
      }, {
        pageName: 'Comics',
        href: '#',
        current: true
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
          <li v-for="(item, index) in menuVoices" :key="index" :class="{'active' : item.current}"><a :href="item.href">{{item.pageName.toUpperCase()}}</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

header{
  height: 120px;
  background-color: #fff;

}

.container{
  @include flex('vertical');
  justify-content: space-between;
}

.logo{
  width: 90px;
}

ul{
  height: 120px;
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
    font-size: .8rem;
    color: $black;
    &:hover{
      color: $blue;
    }
  }
}

</style>
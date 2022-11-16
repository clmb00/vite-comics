<script>

import footerNavContent from '../data/footerMenu';

export default{
  name: 'FooterApp',
  data(){
    return{
      footerNavContent
    }
  }
}
</script>

<template>

  <footer>
    <div class="container">
      <div id="left">
        <nav>
          <div v-for="(section, k) in footerNavContent" :key="k">
            <h3>{{section.sectionName.toUpperCase()}}</h3>
            <ul>
              <li v-for="(item, i) in section.sectionContent" :key="i"><a :href="item.href">{{item.name}}</a></li>
            </ul>
          </div>
        </nav>
      </div>
    </div>
  </footer>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

footer{
  background-color: $l-black;
  background-image: url("../assets/img/footer-bg.jpg");
  background-size: cover;
  .container{
    background-image: url("../assets/img/dc-logo-bg.png");
    background-position: right;
    background-repeat: no-repeat;
  }
  #left{
    padding-block: 20px;
    height: $footer-height;
  }
}

nav{
  @include flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-content: flex-start;
  height: 100%;
  div{
    margin-right: 20px;
    h3{
      font-size: 1.2rem;
      color: white;
      padding-block: 10px;
    }
    ul{
      li{
        padding-block: 1px;
        a{
          color: $grey;
          font-size: .8rem;
          &:hover{
            color: $blue;
          }
        }
      }
    }
  }
}

</style>
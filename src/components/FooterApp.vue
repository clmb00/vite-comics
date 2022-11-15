<script>

import SocialFooter from "./SocialFooter.vue";

export default{
  name: 'FooterApp',
  components:{
    SocialFooter,
  },
  data(){
    return{
      footerNavContent: [
        {
          sectionName: 'Dc Comics',
          sectionContent: [
            {
              name: 'Characters',
              href: '#'
            }, {
              name: 'Comics',
              href: '#'
            }, {
              name: 'Movies',
              href: '#'
            }, {
              name: 'Tv',
              href: '#'
            }, {
              name: 'Games',
              href: '#'
            }, {
              name: 'Videos',
              href: '#'
            }, {
              name: 'News',
              href: '#'
            }
          ]
        }, {
          sectionName: 'Shop',
          sectionContent: [
            {
              name: 'Shop DC',
              href: '#'
            }, {
              name: 'Shop DC Collectibles',
              href: '#'
            }
          ]
        }, {
          sectionName: 'Dc',
          sectionContent: [
            {
              name: 'Yerms of Use',
              href: '#'
            }, {
              name: 'Privacy policy (New)',
              href: '#'
            }, {
              name: 'Ad Choices',
              href: '#'
            }, {
              name: 'Advertising',
              href: '#'
            }, {
              name: 'Jobs',
              href: '#'
            }, {
              name: 'Subscriptions',
              href: '#'
            }, {
              name: 'Talent Workshops',
              href: '#'
            }, {
              name: 'CPSC Certificates',
              href: '#'
            }, {
              name: 'Ratings',
              href: '#'
            }, {
              name: 'Shop Help',
              href: '#'
            }, {
              name: 'Contact Us',
              href: '#'
            }
          ]
        }, {
          sectionName: 'Sites',
          sectionContent: [
            {
              name: 'DC',
              href: '#'
            }, {
              name: 'MAD Magazine',
              href: '#'
            }, {
              name: 'DC Kids',
              href: '#'
            }, {
              name: 'DC Universe',
              href: '#'
            }, {
              name: 'DC Power Visa',
              href: '#'
            }
          ]
        }
      ]
    }
  }
}
</script>

<template>

  <footer>
    <div class="container">
      <div id="top">
        <nav>
          <div v-for="(section, k) in footerNavContent" :key="k">
            <h3>{{section.sectionName.toUpperCase()}}</h3>
            <ul>
              <li v-for="(item, i) in section.sectionContent" :key="i"><a :href="item.href">{{item.name}}</a></li>
            </ul>
          </div>
        </nav>
      </div>
      <div id="bottom">
        <SocialFooter />
      </div>
    </div>
  </footer>

</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

footer{
  background-color: $l-black;
  #top{
    padding-block: 25px;
    height: 320px;
  }
}

nav{
  @include flex;
  flex-direction: column;
  flex-wrap: wrap;
  align-content: flex-start;
  height: 270px;
  div{
    width: fit-content;
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
          font-weight: 500;
          &:hover{
            text-decoration: underline;
          }
        }
      }
    }
  }
}

</style>
<script>

import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import BlueSectionApp from "./components/BlueSectionApp.vue";
import FooterApp from "./components/FooterApp.vue";
import SocialFooter from "./components/SocialFooter.vue";

export default{
  name: 'App',
  components:{
    HeaderApp,
    MainApp,
    BlueSectionApp,
    FooterApp,
    SocialFooter
  }
}
</script>

<template>

  <HeaderApp />
  <MainApp />
  <BlueSectionApp />
  <FooterApp />
  <SocialFooter />

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>

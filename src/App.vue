<script>

import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import BlueSectionApp from "./components/BlueSectionApp.vue";
import FooterApp from "./components/FooterApp.vue";
import FooterSocialApp from "./components/FooterSocialApp.vue";

export default{
  name: 'App',
  components:{
    HeaderApp,
    MainApp,
    BlueSectionApp,
    FooterApp,
    FooterSocialApp
  }
}
</script>

<template>

  <HeaderApp />
  <MainApp />
  <BlueSectionApp />
  <FooterApp />
  <FooterSocialApp />

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>

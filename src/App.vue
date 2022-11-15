<script>

import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import BlueSectionApp from "./components/BlueSectionApp.vue";
import FooterApp from "./components/FooterApp.vue";

export default{
  name: 'App',
  components:{
    HeaderApp,
    MainApp,
    BlueSectionApp,
    FooterApp
  }
}
</script>

<template>

  <HeaderApp />
  <MainApp />
  <BlueSectionApp />
  <FooterApp />

</template>

<style lang="scss">

@use './styles/general.scss' as *;

</style>

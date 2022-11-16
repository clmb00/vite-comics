<script>

import cardMain from './CardMain.vue';

import cardsData from '../data/dc-comics.json';

export default{
  name: 'MainApp',
  components:{
    cardMain
  },
  data(){
    return{
      cardsData,
    }
  }
}

</script>

<template>
  <div id="jumbotron"></div>
  <main>
    <div class="container">
      <h1>Current Seires</h1>
      <div class="card-group">
        <cardMain v-for="(card, index) in cardsData" :key="index" :name="card.series" :thumbUrl="card.thumb"/>
      </div>
      <div class="button-container">
        <button>Load More</button>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;
@use '../styles/partials/mixin' as *;

#jumbotron{
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
  background-position: top;
  height: $jumbo-height;
}

main{
  background-color: $black;
  color: white;
}

.container{
  position: relative;
}

h1, button{
  text-transform: uppercase;
}

h1{
  font-size: 1.8rem;
  padding: 10px 20px;
  background-color: $blue;
  position: absolute;
  transform: translateY(-50%);
}

.card-group{
  @include flex();
  flex-wrap: wrap;
  padding-block: 50px;
  row-gap: 40px;
}

.button-container{
  text-align: center;

  button{
    margin-bottom: 25px;
    padding: 10px 50px;
    border: none;
    background-color: $blue;
    font-size: .8rem;
    color: white;
    font-weight: bold;
    cursor: pointer;
    &:hover{
      filter: brightness(1.2);
    }
  }
}


</style>
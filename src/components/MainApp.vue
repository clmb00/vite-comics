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
      loadedCards: 12
    }
  },
  methods:{
    incrementLoading(){
      if (this.loadedCards + 6 > this.cardsData.length) this.loadedCards = this.cardsData.length;
      else this.loadedCards += 6;
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
        <cardMain v-for="index in loadedCards" :key="index" :name="cardsData[index-1].series" :thumbUrl="cardsData[index-1].thumb"/>
      </div>
      <div class="button-container" v-on:click='incrementLoading'>
        <button> Load More </button>
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
<script>

export default{
  name: 'CardMain',
  props:{
    name: String,
    thumbUrl: String
  }
}

</script>

<template>

<div class="card">
  <div class="cover">
    <img :src="thumbUrl" :alt="name">
  </div>
  <h4>{{name}}</h4>
</div>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.card{
  padding-inline: 10px; 
  width: $width_card;
}

.cover{
  width: 100%;
  aspect-ratio: 1/1;
  img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top;
  }
}

h4{
  margin-top: 10px;
  text-transform: uppercase;
  font-size: .8rem;
}


</style>
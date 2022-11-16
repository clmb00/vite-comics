<script>

export default{
  name: 'CardMain'
}

</script>

<template>

<div class="card">
  <div class="cover">
    <img src="#" alt="">
  </div>
  <h4>Title Comic</h4>
</div>


</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

.card{
  padding-inline: 10px; 
  width: $width_card;
}

.cover{
  background-color: $blue;
  width: 100%;
  aspect-ratio: 1/1;
}

h4{
  margin-top: 10px;
  text-transform: uppercase;
  font-size: .8rem;
}


</style>
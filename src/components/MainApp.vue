<script>

export default{
  name: 'MainApp'
}

</script>

<template>
  <main>
    <div class="container">
      <p>--> Content goes here &lt;--</p>
    </div>
  </main>
</template>

<style lang="scss" scoped>

@use '../styles/partials/variables' as *;

main{
  background-color: $black;
  color: white;
  // debug
  height: 140px;
  line-height: 140px;

  p{
    font-size: 1.8rem;
  }
}

</style>
<template>
  <div class="slogan-container">
    <img class="slogan" alt="slogan" src="../assets/sloganFont.jpg" />
  </div>
</template>


<style lang="sass" scoped>
.slogan-container
  width: 100%
  height: 450px
  margin-top: 10px
  background: url(../assets/sloganBG.png) no-repeat center 75px
  background-size: contain
  text-align: center
  img
    width: 140px
    margin: 80px auto

@media (min-width: 960px)
  .slogan-container
    height: 550px
    margin: 20px 0
    img
      width: 180px
</style>
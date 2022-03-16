<template>
  <div class="entrance-container">
    <img class="entrance" alt="entrance" src="../assets/entrance.jpg" />
    <button class="enter">進入首頁</button>
  </div>
</template>

<style lang="sass" scoped>
.entrance-container
  position: relative
  width: 100%
  height: 100%
.entrance

  z-index: 0
.enter
  position: absolute
  background-color: rgba(0, 0, 0, 0.4)
  color: rgb(255, 255, 255)
  left: 50%
  top: 50%
  width: 15%
  height: 10%
  font-size: 23px
  border-radius: 10px
  transform: translate(-50%, -50%)
  border: none
  opacity: 0.8
</style>
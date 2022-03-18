<template>
  <div class="about">
    <Navbar />
    <div class="img">
      <p>Works</p>
    </div>
    <div class="breadcrumbs">
      <p>首頁/作品集</p>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";


export default {
  name: "Home",
  components: {
    Navbar,
  },
};
</script>

<style lang="sass" scoped>
.img
  display: flex
  margin-top: 86px !important
  background: url(../assets/aboutBG.png) no-repeat center
  width: 100%
  height: 100px
  background-size: cover
  font-size: 28px
  text-shadow: 1px 1px 1px
  justify-content: center
  align-items: center

.breadcrumbs
  width: 100%
  > p
    width: 95%
    margin: 30px auto 0
    color: #698E8E
</style>
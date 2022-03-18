<template>
  <div class="about">
    <div class="wrapper">
      <Navbar />
      <div class="img">
        <p>About Us</p>
      </div>
      <div class="breadcrumbs">
        <p>首頁/關於我們</p>
      </div>
      <AboutContent />
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import AboutContent from "@/components/AboutContent.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    AboutContent,
    Footer,
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

.wrapper
  flex-grow: 1

@media (min-width: 600px)
  .img
    height: 150px
    font-size: 32px
@media (min-width: 991px)
  .img
    height: 200px
    font-size: 36px
  .breadcrumbs
    width: 80%
    margin: 0 auto
@media (min-width: 1440px)
  .img
    height: 300px
    font-size: 40px
</style>
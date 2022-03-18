<template>
  <div class="about">
    <div class="wrapper">
      <Navbar />
      <div class="img">
        <p>Process</p>
      </div>
      <div class="breadcrumbs">
        <p>首頁/服務流程</p>
      </div>
      <ProcessContent />
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import ProcessContent from "@/components/ProcessContent.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "Home",
  components: {
    Navbar,
    ProcessContent,
    Footer,
  },
};
</script>

<style lang="sass" scoped>
.wrapper
  flex-grow: 1
  margin-bottom: 7rem

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
  .portfolio
    width: 80%
    margin: 70px auto 0
@media (min-width: 1440px)
  .img
    height: 300px
    font-size: 40px
</style>
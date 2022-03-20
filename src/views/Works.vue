<template>
  <div class="about">
    <div class="wrapper">
      <Navbar />
      <div class="img">
        <p>Works</p>
      </div>
      <div class="breadcrumbs">
        <p>首頁/作品集</p>
      </div>
      <div class="portfolio">
        <div class="work">
          <router-link class="link" :to="{ name: 'Work', params: { id: 1 } }">
            <img
              class="work-img"
              alt="work-img"
              src="../assets/portfolio-1.jpg"
            />
            <span>日光微風 李宅</span>
          </router-link>
        </div>
        <div class="work">
          <router-link class="link" :to="{ name: 'Work', params: { id: 2 } }">
            <img
              class="work-img"
              alt="work-img"
              src="../assets/portfolio-2.jpg"
            />
            <span>微甜居所 魏宅</span>
          </router-link>
        </div>
        <div class="work">
          <router-link class="link" :to="{ name: 'Work', params: { id: 3 } }">
            <img
              class="work-img"
              alt="work-img"
              src="../assets/portfolio-3.jpg"
            />
            <span>Life。Live 杜宅</span>
          </router-link>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "Home",
  components: {
    Navbar,
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

.portfolio
  display: grid
  position: relative
  margin-top: 30px
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr))
  width: 100%
  grid-gap: 1.5rem
  cursor: pointer
  text-align: center
  .work-img
    width: 100%
    height: 228px
    max-width: 320px
    object-fit: cover
    margin: 0px auto 0
    &:hover
      filter: grayscale(30%)
      filter: contrast(70%)
    + span
      display: block
      max-width: 320px
      margin: 0px auto 0
      padding: 10px 0 10px 6%
      background: url(../assets/arrow@2x.png) no-repeat 290px
      background-color: #eee
      background-size: 7px 12px
      text-align: left
      font-weight: 700

.link
  text-decoration: none
  color: black
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
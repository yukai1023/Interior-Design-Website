<template>
  <div class="work">
    <div class="wrapper">
      <Navbar />
      <div class="img">
        <p>Work</p>
      </div>
      <div class="breadcrumbs">
        <p>首頁/作品</p>
      </div>
      <WorkSlidersShow :initial-img="imgs" />
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import WorkSlidersShow from "@/components/WorkSlidersShow.vue";
import Footer from "@/components/Footer.vue";
const dummyData = {
  work1: [
    { src: require("../assets/work-1.jpg"), id: 1 },
    { src: require("../assets/work-2.jpg"), id: 2 },
    { src: require("../assets/work-3.jpg"), id: 3 },
    { src: require("../assets/work-4.jpg"), id: 4 },
    { src: require("../assets/work-5.jpg"), id: 5 },
  ],
};
export default {
  name: "work",
  components: {
    Navbar,
    WorkSlidersShow,
    Footer,
  },
  data() {
    return {
      imgs: [],
    };
  },
  created() {
    this.fetchImgs();
  },
  methods: {
    async fetchImgs() {
      this.imgs = dummyData.work1;
    },
  },
};
</script>

<style lang="sass" scoped>
.wrapper
  flex-grow: 1

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
@media (min-width: 1440px)
  .img
    height: 300px
    font-size: 40px
</style>

<template>
  <div class="home">
    <div class="wrapper">
      <Navbar />
      <SlidesShow />
      <Slogan />
      <Portfolio />
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import SlidesShow from "@/components/SlidesShow.vue";
import Slogan from "@/components/Slogan.vue";
import Portfolio from "@/components/Portfolio.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "Home",
  components: {
    Navbar,
    SlidesShow,
    Slogan,
    Portfolio,
    Footer,
  },
};
</script>

<style lang="sass" scoped>
.wrapper
  flex-grow: 1; /*可佔滿垂直剩餘的空間*/
</style>

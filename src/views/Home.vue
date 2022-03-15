<template>
  <div class="home">
    <Navbar />
    <SlidesShow />
    <Slogan />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import SlidesShow from "@/components/SlidesShow.vue";
import Slogan from "@/components/Slogan.vue";
export default {
  name: "Home",
  components: {
    Navbar,
    SlidesShow,
    Slogan,
  },
};
</script>

<template>
  <div id="app">
    <div class="slides">
      <transition-group tag="div" :name="transitionName" class="img-boxex">
        <div
          v-for="(img, idx) of imgs"
          :key="idx"
          class="img-box"
          v-show="idx === showImg"
        >
          <img class="showImg" :src="img.src" />
          <div class="arrow">
            <img
              class="arrow-right"
              @click="setShowImg(1)"
              alt="arrow"
              src="../assets/arrow.png"
            />
            <img
              class="arrow-left"
              @click="setShowImg(-1)"
              alt="arrow"
              src="../assets/arrow.png"
            />
          </div>
        </div>
      </transition-group>
    </div>
  </div>
</template>
<script>
const autoPlayInterval = 5000;
export default {
  data() {
    return {
      transitionName: "fade",
      showImg: 0,
      imgsCount: 8,
      imgs: [
        { src: require("../assets/showImg-1.jpg") },
        { src: require("../assets/showImg-2.jpg") },
        { src: require("../assets/showImg-3.jpg") },
        { src: require("../assets/showImg-4.jpg") },
        { src: require("../assets/showImg-5.jpg") },
      ],
    };
  },
  mounted() {
    setInterval(this.setShowImg, autoPlayInterval);
  },
  methods: {
    setShowImg(changeIdx = 1) {
      switch (true) {
        case changeIdx === 1 && this.showImg === this.imgs.length - 1:
          this.showImg = 0;
          break;
        case changeIdx === -1 && this.showImg === 0:
          this.showImg = this.imgs.length - 1;
          break;
        default:
          this.showImg = this.showImg + changeIdx;
          break;
      }
    },
    setShowImgTo(changeIdxTo) {
      this.showImg = changeIdxTo;
    },
  },
};
</script>

<style lang="sass" scoped>
.slides
  margin-top: 86px !important
  .img-boxex
    position: relative
    width: auto
    height: 150px
    max-height: 100%
    .showImg
      max-height: 100%
      max-width: 100%
    .arrow
      max-width: 100%
      max-height: 100%
      cursor: pointer
      .arrow-right
        margin: 0 1rem
        position: absolute
        max-width: 10%
        right: 0
        top: 50%
        background-color: white
        border-radius: 100px
        transform: translate(0%, -50%)
        &:hover
          opacity: 0.7
      .arrow-left
        margin: 0 1rem
        position: absolute
        max-width: 10%
        left: 0
        top: 50%
        background-color: white
        border-radius: 100px
        transform: translate(0%, -50%) scaleX(-1)
        &:hover
          opacity: 0.7

.img-box
  position: absolute

.fade-enter-active,
.fade-leave-active
  transition: opacity .8s

.fade-enter,
.fade-leave-to
  opacity: 0
@media (min-width: 375px)
  .img-boxex
    height: 235px !important
@media (min-width: 475px)
  .img-boxex
    height: 300px !important
@media (min-width: 960px)
  .img-boxex
    &:hover .arrow
      display: block
      animation: fadein 1s ease
    .arrow
      display: none
</style>
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
        </div>
      </transition-group>
      <div class="btn-group">
        <button class="btn prev" @click="setShowImg(-1)">◀</button>
        <div v-for="(img, idx) of imgs" :key="idx" class="img-bottomBox">
          <img
            class="showImg"
            :src="img.src"
            @click="setShowImgTo(img.id - 1)"
          />
        </div>
        <button class="btn next" @click="setShowImg(1)">▶</button>
      </div>
    </div>
    <div class="bottom-content-BG">
      <div class="bottom-content">
        <div class="left-content">
          <img class="interior" alt="" src="../assets/work-1.jpg" />
        </div>
        <div class="right-content">
          <h4>日光微風 李宅</h4>
          <span
            ><br />初冬，讓陽光小精靈伴隨著微風，照開屋主臉上的笑容，並迎接假日的自己。在小窩裡下廚、追劇，偶爾邀請閨蜜來場下午茶。</span
          >
          <p class="setup"><br />格局：兩房兩廳一衛</p>
          <p>
            <br />
            選擇輕柔調子的奶茶色為主色調，使動靜間，闡述著不造作的優柔氣韻。
            入口利用巧妙設計隱藏電箱，並規劃櫃體分割出玄關及廚房之空間。<br /><br />主臥設計曲面天花，視覺上是弱化樑，同時想帶給屋主空間上的柔和。
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    initialImg: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      transitionName: "fade",
      showImg: 0,
      imgsCount: 8,
      imgs: this.initialImg,
    };
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
  width: 80%
  margin: 0 auto
  .img-boxex
    position: relative
    width: auto
    height: 150px
    max-height: 100%
    .showImg
      max-width: 100%

.img-bottomBox
  position: relative
  width: auto
  max-height: 100%
  .showImg
    max-height: 100%
    max-width: 100%
    padding: 0 10px
    cursor: pointer

.bottom-content-BG
  margin-top: 50px
  width: 100%
  height: 750px
  background-color: #F0EBE5
  .bottom-content
    width: 80%
    margin: 0 auto
    .left-content
      padding-top: 100px
      margin-bottom: 3rem
      .interior
        display: block
        max-width: 320px
        object-fit: cover
        margin: auto
        box-shadow: 12px 12px 12px rgba(0, 0, 0, 0.7)
    .right-content
      .setup
        color: gray
        font-size: 18px

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
@media (min-width: 575px)
  .img-boxex
    height: 370px !important
@media (min-width: 675px)
  .img-boxex
    height: 440px !important
@media (min-width: 775px)
  .img-boxex
    height: 510px !important
@media (min-width: 875px)
  .img-boxex
    height: 580px !important
@media (min-width: 960px)
  .img-boxex
    display: flex
    justify-content: center
    margin: 0 0 50px 0
    .showImg
      object-fit: cover
      height: 600px
      width: 100%
      margin: 0 auto
      max-width: 100%
    .arrow
      display: none
      .arrow-right
        width: 5%
      .arrow-left
        width: 5%
</style>
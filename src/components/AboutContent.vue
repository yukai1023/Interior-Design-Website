<template>
  <div class="About-container">
    <div class="top-content">
      <div class="left-content">
        <h4>傾聽與滿足您的需求，拚盡全力，只為看到您滿意的笑容。</h4>
        <span
          >創立於2021年，位於新竹竹北，具備豐富設計經驗。我們善於傾聽、耐心溝通，為業主梳理需求，過濾出真正合適、好用、耐久居的方式，配合品質精良的工程夥伴，進而實現空間規劃的最大價值。</span
        >
      </div>
      <div class="right-content">
        <img class="company" alt="" src="../assets/aboutCompany.jpg" />
      </div>
    </div>
    <div class="bottom-content-BG">
      <div class="bottom-content">
        <div class="left-content">
          <img class="interior" alt="" src="../assets/aboutInterior.jpg" />
        </div>
        <div class="right-content">
          <h4>
            嚴謹的標準工學，創造舒適的人性空間
            以室內美學的概念，結合使用者及空間的設計。
          </h4>
          <span
            >叶舍空間製作所主要提供給業主專業設計及工程管理，服務範圍包含住宅、商業空間、建築設計、室內設計。
            <br /><br />承續對設計的熱情與工程精緻度的要求，提供業主完整且細膩的服務，呈現創新風格與質感兼具的生活空間。</span
          >
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="sass" scoped>
.About-container
  width: 100%
  margin-top: 30px
  .top-content
    .left-content
      width: 95%
      margin: 0 auto
      h4
        margin-bottom: 2rem
      > span
        color: gray
    .right-content
      margin-top: 20px
      width: 100%
      .company
        display: block
        margin: auto
        height: 450px
        box-shadow: 12px 12px 12px rgba(0, 0, 0, 0.7)
  .bottom-content-BG
    margin-top: 50px
    width: 100%
    height: 650px
    background-color: #F0EBE5
    .left-content
      padding-top: 50px
      margin-bottom: 3rem
      .interior
        display: block
        max-width: 320px
        object-fit: cover
        margin: auto
        box-shadow: 12px 12px 12px rgba(0, 0, 0, 0.7)
    .right-content
      width: 95%
      margin: 0 auto
      h4
        margin-bottom: 2rem
      > span
        color: gray
@media (min-width: 991px)
  .About-container
    width: 100%
    margin-top: 30px
    .top-content
      display: flex
      width: 80%
      margin: 0 auto
      .left-content
        width: 120%
        padding: 50px 0 0 30px
      .right-content
        width: 80%
    .bottom-content-BG
      .bottom-content
        display: flex
        width: 80%
        margin: 30px auto 0
        padding-top: 50px
        .left-content
          width: 80%
          .interior
            max-width: 500px
            margin: 0
        .right-content
          margin: 100px 0 0 50px
          width: 80%

@media (min-width: 1440px)
  .About-container
    .bottom-content-BG
      .right-content
        margin: 100px 0 0 0 !important
        width: 80%
</style>
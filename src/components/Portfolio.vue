<template>
  <div class="portfolio-container">
    <div class="portfolio-bg">
      <img class="logo" alt="logo" src="../assets/logo.png" />
      <p>PORTFOLIO</p>
      <span>精選作品</span>
      <div class="portfolio">
        <div class="work">
          <img
            class="work-img"
            alt="work-img"
            src="../assets/portfolio-1.jpg"
          />
          <span>日光微風 李宅</span>
        </div>
        <div class="work">
          <img
            class="work-img"
            alt="work-img"
            src="../assets/portfolio-2.jpg"
          />
          <span>微甜居所 魏宅</span>
        </div>
        <div class="work">
          <img
            class="work-img"
            alt="work-img"
            src="../assets/portfolio-3.jpg"
          />
          <span>Life。Live 杜宅</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="sass" scoped>
.portfolio-container
  width: 100%
  .portfolio-bg
    background: url(../assets/portfolioBG.png) no-repeat center 40px
    height: 100%
    background-size: 100% 345px
    text-align: center
    .logo
      width: 70px
      margin-top: 80px
    p
      margin: 10px 0 10px 0
      font-size: 24px
      font-weight: 700
      + span
        margin-top: 30px
        font-size: 18px
        color: gray
    .portfolio
      display: grid
      position: relative
      margin-top: 30px
      grid-template-columns: repeat(auto-fit, minmax(350px, 1fr))
      width: 100%
      grid-gap: 1.5rem
      cursor: pointer
      .work-img
        width: 100%
        height: 228px
        max-width: 320px
        object-fit: cover
        margin: 0px auto 0
        &:hover
          opacity: 0.7
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
</style>
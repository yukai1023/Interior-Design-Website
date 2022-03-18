<template>
  <div class="process-container">
    <div class="title">
      <h3>服務流程</h3>
      <span>面對面了解</span>
    </div>
    <div class="process">
      <div class="process-left">
        <div class="left-content">
          <div class="number">1</div>
          <div class="content">
            <h6>接案初步詢問</h6>
            <p>．了解個案環境，詢問客戶需求</p>
            <p>．現場丈量勘景，拍照</p>
            <p>．繪製現況平面圖</p>
          </div>
        </div>
        <div class="left-content">
          <div class="number">2</div>
          <div class="content">
            <h6>設計草圖規劃</h6>
            <p>．討論提案簡報</p>
            <p>．含「平面配置圖」、「空間風格」</p>
            <p>．評估約略工程花費及建議</p>
            <p>．設計費報價簽名及付費</p>
          </div>
        </div>
      </div>
      <div class="process-img">
        <img class="img" alt="" src="../assets/processImg.jpg" />
      </div>
      <div class="process-right">
        <div class="right-content">
          <div class="number">3</div>
          <div class="content">
            <h6>委託細部設計</h6>
            <p>．繪製平、立面系統圖及材質討論</p>
            <p>．免費提供空間簡易3D圖(無擬真效果)</p>
            <p>．編列工程預算估計討論</p>
          </div>
        </div>
        <div class="right-content">
          <div class="number">4</div>
          <div class="content">
            <h6>施工監工委託簽約</h6>
            <p>．工程整體報價確認及簽訂</p>
            <p>．工程管理費</p>
            <p>．排定工期及細目，進場施工</p>
            <p>．施工進度回報</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>


<style lang="sass" scoped>
.process-container
  width: 100%
  margin-top: 10px
  .title
    position: relative
    width: 100%
    height: 230px
    text-align: center
    &:before
      content: ''
      width: 1.5px
      height: 70px
      background-color: #af9f66
      position: absolute
      bottom: 40px
    > h3
      margin: 60px auto 30px
    > span
      color: #999
  .process
    margin: 0 auto
    .process-left
      width: 80%
      margin: 0 auto
      .left-content
        display: flex
        margin-bottom: 50px
        .number
          font-size: 45px
          color: #af9f66
        .content
          letter-spacing: 0em
          color: #5E5A54
          font-size: 15px
          padding-left: 20px
          > h6
            color: black
    .process-img
      text-align: center
      width: 100%
      margin-bottom: 50px
      .img
        width: 350px
        height: 350px
        border-radius: 50%
    .process-right
      width: 80%
      margin: 0 auto
      .right-content
        display: flex
        margin-bottom: 50px
        .number
          font-size: 45px
          color: #af9f66
        .content
          letter-spacing: 0em
          color: #5E5A54
          font-size: 15px
          padding-left: 20px
          > h6
            color: black

@media (min-width: 991px)
  .process
    display: flex
    width: 80%
    margin: 0 auto
    .process-left
      .left-content
        margin-bottom: 150px !important
    .process-img
      margin-left: 110px !important
    .process-right
      margin-left: 110px !important
      .right-content
        margin-bottom: 150px !important
</style>

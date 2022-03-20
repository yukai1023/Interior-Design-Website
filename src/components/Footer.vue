<template>
  <footer class="footer">
    <div class="inner">
      <div class="left-inner">
        <p class="title"><strong>叶舍空間製作所</strong></p>
        <div class="content">
          <p>302 新竹縣竹北市新竹縣竹北市莊敬五街131號2F</p>
          <p class="telephone">03 658-6883</p>
          <p class="email">yhousedesign2021@gmail.com</p>
          <p class="time">AM9 ~ PM6 (六、日及國定假日公休)</p>
        </div>
      </div>
      <div class="right-inner">
        <p class="title"><strong>Follow Us</strong></p>
        <div class="content">
          <a href="https://www.facebook.com/yhousedesign/?ref=page_internal"
            ><img class="icon" alt="icon" src="../assets/icon-Facebook.png"
          /></a>
          <a href="https://www.instagram.com/yhousedesign/">
            <img class="icon" alt="icon" src="../assets/icon-Instagram.png"
          /></a>
        </div>
      </div>
    </div>
    <div class="bottom">
      <p>©2022 Yhouse Inc. All rights reserved.</p>
    </div>
  </footer>
</template>


<style lang="sass" scoped>
.footer
  position: relative
  width: 100%
  height: 250px
  background-color: #333
  .inner
    width: 90%
    margin: 0 auto
    color: #fff
    padding: 35px 0 0px
    .left-inner
      .title
        letter-spacing: 3px
      .content
        margin-top: 10px
        font-size: 12px
        letter-spacing: 3px
        p
          margin-top: 5px
        .telephone
          padding-left: 30px
          background: url(../assets/icon-Telephone.png) no-repeat
          background-size: 20px 20px
          height: 20px
        .email
          padding-left: 30px
          background: url(../assets/icon-Email.png) no-repeat
          background-size: 20px 20px
          height: 20px
        .time
          padding-left: 30px
          background: url(../assets/icon-Time.png) no-repeat
          background-size: 18px 18px
          height: 20px
    .right-inner
      margin-top: 10px
      .title
        letter-spacing: 3px
      .content
        display: flex
        .icon
          cursor: pointer
          margin: 10px 20px 0 0
          height: 30px
  .bottom
    position: absolute
    color: #fff
    font-size: 12px
    right: 5px
    bottom: 10px

@media (min-width: 960px)
  .footer
    height: 190px
    .inner
      display: flex
      width: 60%
      .left-inner
        width: 70%
      .right-inner
        margin: 0
        width: 30%
    .bottom
      right: 30px
      bottom: 10px
</style>
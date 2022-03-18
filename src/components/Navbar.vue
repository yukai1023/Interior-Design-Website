// ./src/components/Navbar.vue

<template>
  <nav
    class="
      navbar navbar-expand-lg
      fixed-top
      navbar-dark
      bg-dark
      shadow-sm
      p-2
      mb-5
      bg-body
    "
  >
    <div class="logo-container">
      <router-link
        class="logo-link"
        :to="{
          name: 'Home',
        }"
      >
        <img class="logo" alt="logo" src="../assets/logo.png" />
        <img class="logoFont" alt="logoFont" src="../assets/logoFont.png" />
      </router-link>
    </div>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon" />
    </button>

    <div id="navbarSupportedContent" class="navbar-collapse collapse">
      <div class="ml-auto d-flex align-items-center">
        <router-link
          class="font"
          :to="{
            name: 'Home',
          }"
        >
          首頁
        </router-link>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <router-link
          class="font"
          :to="{
            name: 'About',
          }"
        >
          關於我們
        </router-link>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <router-link
          class="font"
          :to="{
            name: 'Works',
          }"
        >
          作品集
        </router-link>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <router-link
          class="font"
          :to="{
            name: 'Process',
          }"
        >
          服務流程
        </router-link>
      </div>
    </div>
  </nav>
</template>

<style lang="sass" scoped>
.navbar-toggler
  min-width: 70px
  margin-right: 0
  background-color: gray
  border-color: white !important

.logo-container
  display: flex
  .logo
    width: 70px
    border: none
  .logoFont
    width: 180px
    object-fit: fill
    object-fit: contain
    object-fit: scale-down

nav.bg-dark
  padding: 0px 16px
  background-color: white !important

.navbar-brand
  font-size: 19px
  padding: 0

.align-items-center
  cursor: pointer
  border-top: 1px solid #E6ECF0
  height: 70px
  justify-content: center
  font-weight: 700
  letter-spacing: 3px
  font-size: 18px
  .font
    text-decoration: none
    color: black

.router-link-exact-active
  color: #CF8A08 !important
@media (min-width: 991px)
  .navbar
    padding: 0.5rem 13% !important
  .align-items-center
    border-top: none
    height: 50px
    .font
      &:hover
        color: #CF8A08 !important
        border-bottom: 3px solid #CF8A08
        transition: all .5s ease
  .router-link-exact-active
    color: #CF8A08 !important
    border-bottom: 3px solid #CF8A08
  .logo-link
    border: none
</style>
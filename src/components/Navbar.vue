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
      <img class="logo" alt="logo" src="../assets/logo.png" />
      <img class="logoFont" alt="logoFont" src="../assets/logoFont.png" />
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
        <p>首頁</p>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <p>關於我們</p>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <p>作品集</p>
      </div>
      <div class="ml-auto d-flex align-items-center">
        <p>客戶服務</p>
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
</style>
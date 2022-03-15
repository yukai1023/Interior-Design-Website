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
        <!-- is user is admin -->
        <router-link to="/admin/restaurants" class="text-white mr-3">
          管理員後台
        </router-link>

        <template>
          <router-link to="#" class="text-white mr-3"> 您好 </router-link>
          <button
            type="button"
            class="btn btn-sm btn-outline-success my-2 my-sm-0"
            @click="logout"
          >
            登出
          </button>
        </template>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    logout() {
      this.$store.commit("revokeAuthentication");
      this.$router.push("/signin");
    },
  },
};
</script>

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
</style>
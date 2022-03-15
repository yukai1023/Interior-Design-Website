<template>
  <div id="restaurant-forum">
    <main role="main" class="bg-white">
      <router-view />
    </main>
  </div>
</template>

<script>
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";

export default {
  name: "App",
};
</script>

<style>
#app {
  font-family: "Noto Sans TC";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}


#nav a.router-link-exact-active {
  color: #42b983;
}

p {
  margin: 0;
}
</style>

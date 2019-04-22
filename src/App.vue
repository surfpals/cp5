<template>
<div id="app">
  <div class="pure-menu">
    <span class="pure-menu-heading">The Internets Task System</span>
      <p></p>
      <router-link to="/" class="pure-menu-link">Home</router-link> |
      <router-link to="/LoggingIn" class="pure-menu-link">Login</router-link> |
      <router-link to="/About" class="pure-menu-link">About</router-link>
      <br>
      <br>
  </div>
  <div class="content">
  <router-view />
  </div>
</div>
</template>


<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding-bottom: 20px;
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
</style>

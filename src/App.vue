<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">PokéDex</router-link> <br>
      <router-link to="/myTeam">My Team</router-link> <br>
      <router-link to="/savedTeams">Saved Teams</router-link> <br>
      <a @click="loginStatus = !loginStatus;">Log In</a> <br>
      <p v-if="!loginStatus">IT WORKS</p>
    </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  text-align: left;
  background-color: red;
  margin-bottom: -350px;
  padding-top: 190px;
  margin-left: 26px;
  line-height: 40pt;
  z-index: -1000;
}

#nav a {
  font-weight: bold;
  color: black;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: rgb(77, 77, 77);
}
#nav a.router-link-exact-active:hover {
  margin-left: 0px;
  color: rgb(77, 77, 77);
}
#nav a:hover {
  font-weight: bold;
  color: red;
  margin-left: 2px;
}
</style>

<script>

export default {
  data: () => {
    return {
      loginStatus: true
    }
  }
}
</script>

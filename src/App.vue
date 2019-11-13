<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">PokéDex</router-link> |
      <router-link to="/myTeam">My Team</router-link>
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
  background-color: white;
}
#nav {
  padding: 30px;
  margin-left: 7%;
  margin-bottom: -2%;
  background-color: red;
}

#nav a {
  font-weight: bold;
  color: #632525;
}

#nav a.router-link-exact-active {
  color: white;
}
#nav a:hover {
  font-weight: bold;
  color: #000000;
}
</style>
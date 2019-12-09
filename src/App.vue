<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">PokéDex</router-link> <br>
      <router-link to="/team">My Team</router-link> <br>
      <router-link v-if="nameArray.length == 6"
      to="/types">Type Analysis</router-link> 
      <a v-if="nameArray.length != 6"
      @click="typeStatus = !typeStatus;"
      >Type Analysis</a>
    </div>
    <router-view/>
    <div id="type-box" v-if="typeStatus">
      <div id="type-box-inner">
        <p>You must complete a team for type analysis! <br>{{nameArray.length}}/6 Pokémon</p><br>
            <v-btn style="background-color: red; color: white; margin: auto; width: 80%; margin-top: 10px; margin-bottom: 10px;"
            @click="typeStatus = false;"
            >
            Okay
            </v-btn>
      </div>
    </div>
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
  margin-bottom: -402px;
  padding-top: 240px;
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
#type-box {
    background-color: rgb(0, 0, 0, 0.5); 
    z-index: 1000; 
    position: fixed; 
    top: 0; 
    left: 0; 
    height: 100%; 
    width: 100%;
    overflow: hidden;
    
}
#type-box-inner {
    background-color: white; 
    margin: auto; 
    width: 30%; 
    margin-top: 20%; 
    padding: 10px;
}
</style>

<script>

export default {
  data: () => {
    return {
      typeStatus: false
    }
  },
    computed: {
      nameArray() {
          return this.$store.state.teamName;
      }
  }
}
</script>
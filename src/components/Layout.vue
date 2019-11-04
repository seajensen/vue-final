<template>
<body>
<div id="right-side">
    <div id="header-div">
        <img id="icon" src="../assets/pokeball.png">
        <h1 id="h1Title">PokéDex</h1>
    </div>
    <v-content>
        <pk-box :pkmon="pkmon"></pk-box>
    </v-content>

<v-footer id="footer-div">
    <p>Made for educational purposes.</p>
</v-footer>
</div>
</body>
</template>

<script>
import PkBox from './PkBox';

export default {
  props: ["pkmon"],
  data: () => ({
    name: "Sean",
  }),
  components: {
      PkBox,
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Bowlby+One&display=swap');

body {
    background-color: white;
    height: 120%;
}
#header-div {
    display: flex;
}
h1 {
    color: white;
    font-family: 'Bowlby One', cursive;
    font-size: 60pt;
    text-align: center;
    margin: auto;
}
#h1Title {
    margin-top: -1px;
    padding-right: 100px;
    padding-top: 40px;
}
#right-side {
    background-color: red;
    height: 100%;
    margin-left: 7%;
}
#icon {
    width: 200px;
    margin-left: -100px;
}
#footer-div {
    height: 30px;
    margin-bottom: 0px;
    color: grey;
    background-color: white;
}
</style>




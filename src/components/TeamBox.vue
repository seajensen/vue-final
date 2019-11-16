<template>
<div id="dex-box">
    <p>Click on a Pokémon to Learn More</p><br>
    <div id="TeamDisplay">
        <p>Name: {{ name[0] }}, {{ height[0] }}, {{ weight[0] }}, {{ sprite[0] }}, {{ length }}</p>
    </div>
    <div style="display: flex;">
        <img :src="sprite[0]">
        <v-btn style="background-color: red; color: white; margin: auto; width: 120px;"
        @click="infoCheck()"
        >{{ name[0] }}</v-btn>
    </div>
    <div style="background-color: rgb(221, 221, 221);" v-if="infoToggle">
        <p>Type(s): {{ type[0] }}</p>
        <v-divider></v-divider>
        <p>Height: {{ height[0] }}</p>
        <v-divider></v-divider>
        <p>Weight: {{ weight[0] }}</p>
        <v-divider></v-divider>
        <v-btn style="background-color: red; color: white; margin: auto; width: 90%; margin-top: 10px; margin-bottom: 10px;"
        @click="infoCheck()"
        >
            Remove from Team
        </v-btn>
    </div>
</div>
</template>


<script>
import PkComp from './PkComp';

export default {
  data: () => ({
    infoToggle: false,
  }),
  computed: {
      type() {
          return this.$store.state.teamType;
      },
      height() {
          return this.$store.state.teamHeight;
      },
      weight() {
          return this.$store.state.teamWeight;
      },
      name() {
          return this.$store.state.teamName;
      },
      sprite() {
          return this.$store.state.teamSprite;
      },
      length() {
          return this.$store.state.teamName.length;
      }

  },
  methods: {
      infoCheck() {
          if(this.infoToggle == false) {
            this.infoToggle = true;
          } else {
            this.infoToggle = false;
          }
      }
  }
};
</script>


<style scoped>
#dex-box {
    background-color: white;
    width: 70%;
    padding-bottom: 15px;
    padding-right: 5px;
    margin: auto;
    margin-bottom: 100px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}
#dex-box img {
    margin-bottom: -1000px;
}
.pkBtn {
    background-color: red;
}
p {
    text-align: center;
    width: 100%;
    margin-top: 15px;
}
</style>



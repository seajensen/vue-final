<template>
<div id="dex-box">
    <div id="TeamDisplay" v-for="count in count" :key="count" v-if=name[count]
    style="padding-top: 20px;">
    <div style="display: flex;">
        <img :src="sprite[count]"
        style="max-height: 90px; margin-top: -28px;"
        >
        <h2>{{ name[count] }}</h2>
    </div>
    <div style="background-color: rgb(221, 221, 221);">
        <p>Type(s): {{ type[count] }}</p>
        <v-divider></v-divider>
        <p>Height: {{ height[count] }}</p>
        <v-divider></v-divider>
        <p>Weight: {{ weight[count] }}</p>
        <v-divider></v-divider>
        <v-btn style="background-color: red; color: white; margin: auto; width: 90%; margin-top: 10px; margin-bottom: 10px;"
        @click="teamRelease(count)"
        >
            Release Pokémon
        </v-btn>
    </div>
    </div>
    <div v-if=!name[0]>
        <p>This team is currently empty</p>
    </div>
</div>
</template>


<script>
import PkComp from './PkComp';

export default {
  data: () => ({
      count: [0, 1, 2, 3, 4, 5]
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
      }

  },
  methods: {
      teamRelease(a) {
          this.$store.state.teamType.splice(a,1);
          this.$store.state.teamHeight.splice(a,1);
          this.$store.state.teamWeight.splice(a,1);
          this.$store.state.teamName.splice(a,1);
          this.$store.state.teamSprite.splice(a,1);
          this.$store.state.teamCount--;
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



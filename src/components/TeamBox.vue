<template>
<div id="dex-box">
    <div v-if=name[0]
    style="width: 100%;"
    >
    <h2>{{newTeamName}}</h2>
    </div>
    <div id="TeamDisplay" v-for="count in count" :key="count" v-if=name[count]
    style="padding-top: 20px; margin: 0px 5px;">
    <div style="display: flex;">
        <img :src="sprite[count]"
        style="max-height: 90px; margin-top: -28px;"
        >
        <h2>{{ name[count] }}</h2>
    </div>
    <div style="background-color: rgb(221, 221, 221); min-width: 230px;">
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
    <div v-if=name[0]
    style="width: 100%; display: flex; margin-left: 8%;"
    >
    <br>
    <label style="margin-top: 13px; margin-right: 10px;">Team Name: </label>
    <div>
        <input type="text" style="border: 1px solid black; margin-top: 14px;" v-model="myTeamName">
        <p v-if="errors.length" style="font-size: 8pt; margin-top: 0px; color: red;">
            <ul>
                <li v-for="error in errors" style="list-style: none;">{{ error }}</li>
            </ul>
        </p>
    </div>
    <v-btn style="background-color: red; color: white; margin: auto; margin-left: 10px; margin-top: 8px;"
    @click="teamNameBtn">
        Update Name
    </v-btn>
    <v-btn style="background-color: red; color: white; margin: auto; margin-left: 0px; margin-top: 8px;"
    @click="randomName">
        Random Name
    </v-btn>
    </div>
</div>
</template>


<script>
import PkComp from './PkComp';

export default {
  data: () => ({
      count: [0, 1, 2, 3, 4, 5],
      myTeamName: '',
      newTeamName: '',
      teamArray: [],
      errors: []
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
      randomNum() {
          let x = (Math.random() * 6);
          return x;
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
      },
      teamNameBtn() {
          console.log(this.myTeamName);
          this.errors = [];
          if(this.myTeamName.length > 12) {
            this.errors.push("Please use fewer characters");
          } else if(this.myTeamName.includes('thor')) {
            this.errors.push("You can be more creative, Thor");
          } else if(this.myTeamName.includes('Thor')) {
            this.errors.push("You can be more creative, Thor");
          } else {
              this.newTeamName = this.myTeamName;
          }
      },
      randomName() {
          this.$http.get('https://pokedex-80157.firebaseio.com/test.json')
          .then(response => {
              return response.json();
          })
          .then(data => this.teamArray = data);
          let x = Math.floor(Math.random() * 6)
          this.newTeamName = this.teamArray[x];
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



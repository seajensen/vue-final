<template>
<div>
    <div style="display: flex;">
        <img :src="pkmon.sprites.front_default" :id="pkmon.id">
        <v-btn style="background-color: red; color: white; margin: auto; width: 120px;"
        @click="pkmonInfo(pkmon.height, pkmon.weight, pkmon.types)"
        >{{ pkmon.name }}</v-btn>
    </div>
    <div style="background-color: rgb(221, 221, 221);" v-if="infoToggle">
        <p>Type(s): {{pkmonType}}</p>
        <v-divider></v-divider>
        <p>Height: {{pkmonHeight}}</p>
        <v-divider></v-divider>
        <p>Weight: {{pkmonWeight}}</p>
        <v-divider></v-divider>
        <v-btn style="background-color: red; color: white; margin: auto; width: 80%; margin-top: 10px; margin-bottom: 10px;"
        @click="teamAdd(pkmonType, pkmonHeight, pkmonWeight, pkmon.name, pkmon.sprites.front_default)"
        >
            Add to My Team
        </v-btn>
    </div>
    <div v-if="teamFull"
        id="fullteam-alert"
    >   
        <div id="alert-inner">
            <p>Your team is full! Please release a Pokémon before you add a new one!</p><br>
            <v-btn style="background-color: red; color: white; margin: auto; width: 80%; margin-top: 10px; margin-bottom: 10px;"
            @click="teamFull = false;"
            >
            Okay
            </v-btn>
        </div>
    </div>
</div>
</template>


<script>

export default {
  props: {
      pkmon: {
          type: Object,
      },
  },
  methods: {
        pkmonInfo(a, b, c) {
          if(this.infoToggle == false) {
            this.pkmonHeight = a;
            this.pkmonWeight = b;
            if(c.length > 1)
                {
                    this.pkmonType = c[0].type.name + "/" + c[1].type.name;
                } else {
                    this.pkmonType = c[0].type.name;
                }
            this.infoToggle = true;
          } else if(this.infoToggle == true) {
            this.infoToggle = false;
          }

      },
      teamAdd(a, b, c, d, e) {
          if(this.$store.state.teamCount < 6) {
            this.$store.state.teamType.push(a);
            this.$store.state.teamHeight.push(b);
            this.$store.state.teamWeight.push(c);
            this.$store.state.teamName.push(d);
            this.$store.state.teamSprite.push(e);
            this.$store.state.teamCount++;
          } else {
              this.teamFull = true;
          }
          
      }
  },
    computed: {
      length() {
          return this.$store.state.teamName.length;
      }
  },
  data: () => ({
    pkmonType: null,
    pkmonHeight: null,
    pkmonWeight: null,
    infoToggle: false,
    teamCount: 0,
    teamFull: false,
  })
};
</script>


<style>
#fullteam-alert {
    background-color: rgb(0, 0, 0, 0.5); 
    z-index: 1000; 
    position: fixed; 
    top: 0; 
    left: 0; 
    height: 100%; 
    width: 100%;
    overflow: hidden;
}
#alert-inner {
    background-color: white; 
    margin: auto; 
    width: 30%; 
    margin-top: 20%; 
    padding: 10px;
}
</style>

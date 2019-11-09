<template>
<div>
    <div style="display: flex;">
        <img :src="pkmon.sprites.front_default" :id="pkmon.name">
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
          console.log(a);
          console.log(b);
          console.log(c);
          console.log(d);
          console.log(e);
      }
  },
  data: () => ({
    pkmonType: null,
    pkmonHeight: null,
    pkmonWeight: null,
    infoToggle: false,
  })
};
</script>


<style>

</style>

<template>
<div id="dex-box">
    <div style="display: flex; justify-content: space-around;">
        <img :src="sprite[0]"><p>{{pktype[0]}}</p>
        <p>{{types[0].name}}</p>
        <p v-if="typeAnalysis[0] != 'x'">{{types[typeAnalysis[0]].name}}</p>
        <p v-if="typeAnalysis[1] != 'x'">{{types[typeAnalysis[1]].name}}</p>
        <p v-if="typeAnalysis[2] != 'x'">{{types[typeAnalysis[2]].name}}</p>
        <p v-if="typeAnalysis[3] != 'x'">{{types[typeAnalysis[3]].name}}</p>
        <p v-if="typeAnalysis[4] != 'x'">{{types[typeAnalysis[4]].name}}</p>
        <p v-if="typeAnalysis[5] != 'x'">{{types[typeAnalysis[5]].name}}</p>
        <p v-if="typeAnalysis[6] != 'x'">{{types[typeAnalysis[6]].name}}</p>
        <p v-if="typeAnalysis[7] != 'x'">{{types[typeAnalysis[7]].name}}</p>
        <p v-if="typeAnalysis[8] != 'x'">{{types[typeAnalysis[8]].name}}</p>
        <p v-if="typeAnalysis[9] != 'x'">{{types[typeAnalysis[9]].name}}</p>
        <p v-if="typeAnalysis[10] != 'x'">{{types[typeAnalysis[10]].name}}</p>
        <p v-if="typeAnalysis[11] != 'x'">{{types[typeAnalysis[11]].name}}</p>
    </div>
</div>
</template>


<script>
import { types } from '../assets/type.js'

export default {
  data: () => ({
      typeObject: null,
      types: types,
      pk1: null,
      pk2: null,
      pk3: null,
      pk4: null,
      pk5: null,
      pk6: null,
      pk11: null,
      pk21: null,
      pk31: null,
      pk41: null,
      pk51: null,
      pk61: null
  }),
  computed: {
      pktype() {
          return this.$store.state.teamType;
      },
      name() {
          return this.$store.state.teamName;
      },
      sprite() {
          return this.$store.state.teamSprite;
      },
      typeAnalysis() {
          let typeArray = [];
          for (let i = 0; i < this.pktype.length; i++) {
                if (this.pktype[i].length < 9) {
                    if(this.pktype[i] == "normal") {
                        typeArray.push(0);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "fighting") {
                        typeArray.push(1);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "flying") {
                        typeArray.push(2);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "poison") {
                        typeArray.push(3);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "ground") {
                        typeArray.push(4);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "rock") {
                        typeArray.push(5);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "bug") {
                        typeArray.push(6);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "ghost") {
                        typeArray.push(7);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "steel") {
                        typeArray.push(8);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "fire") {
                        typeArray.push(9);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "water") {
                        typeArray.push(10);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "grass") {
                        typeArray.push(11);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "electric") {
                        typeArray.push(12);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "psychic") {
                        typeArray.push(13);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "ice") {
                        typeArray.push(14);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "dragon") {
                        typeArray.push(15);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "dark") {
                        typeArray.push(16);
                        typeArray.push("x");
                    } else if(this.pktype[i] == "fairy") {
                        typeArray.push(17);
                        typeArray.push("x");
                    }
                } else {
                    let res = this.pktype[i].split("/");
                    if(res[0] == "normal") {
                        typeArray.push(0);
                    } else if(res[0] == "fighting") {
                        typeArray.push(1);
                    } else if(res[0] == "flying") {
                        typeArray.push(2);
                    } else if(res[0] == "poison") {
                        typeArray.push(3);
                    } else if(res[0] == "ground") {
                        typeArray.push(4);
                    } else if(res[0] == "rock") {
                        typeArray.push(5);
                    } else if(res[0] == "bug") {
                        typeArray.push(6);
                    } else if(res[0] == "ghost") {
                        typeArray.push(7);
                    } else if(res[0] == "steel") {
                        typeArray.push(8);
                    } else if(res[0] == "fire") {
                        typeArray.push(9);
                    } else if(res[0] == "water") {
                        typeArray.push(10);
                    } else if(res[0] == "grass") {
                        typeArray.push(11);
                    } else if(res[0] == "electric") {
                        typeArray.push(12);
                    } else if(res[0] == "psychic") {
                        typeArray.push(13);
                    } else if(res[0] == "ice") {
                        typeArray.push(14);
                    } else if(res[0] == "dragon") {
                        typeArray.push(15);
                    } else if(res[0] == "dark") {
                        typeArray.push(16);
                    } else if(res[0] == "fairy") {
                        typeArray.push(17);
                    };
                    if(res[1] == "normal") {
                        typeArray.push(0);
                    } else if(res[1] == "fighting") {
                        typeArray.push(1);
                    } else if(res[1] == "flying") {
                        typeArray.push(2);
                    } else if(res[1] == "poison") {
                        typeArray.push(3);
                    } else if(res[1] == "ground") {
                        typeArray.push(4);
                    } else if(res[1] == "rock") {
                        typeArray.push(5);
                    } else if(res[1] == "bug") {
                        typeArray.push(6);
                    } else if(res[1] == "ghost") {
                        typeArray.push(7);
                    } else if(res[1] == "steel") {
                        typeArray.push(8);
                    } else if(res[1] == "fire") {
                        typeArray.push(9);
                    } else if(res[1] == "water") {
                        typeArray.push(10);
                    } else if(res[1] == "grass") {
                        typeArray.push(11);
                    } else if(res[1] == "electric") {
                        typeArray.push(12);
                    } else if(res[1] == "psychic") {
                        typeArray.push(13);
                    } else if(res[1] == "ice") {
                        typeArray.push(14);
                    } else if(res[1] == "dragon") {
                        typeArray.push(15);
                    } else if(res[1] == "dark") {
                        typeArray.push(16);
                    } else if(res[1] == "fairy") {
                        typeArray.push(7);
                    };
                }
            }
          return typeArray;
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
img {
    height: 150px;
    width: 240px;
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



<template>
<div id="dex-box">
    <div style="width: 100%;">
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[0]">
                    <p>{{name[0]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[0]" class="typeImg">
                <p>{{types[typeAnalysis[0]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[0]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[0]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[1] != 'x'">
                <img :src="typeImg[1]" class="typeImg">
                <p>{{types[typeAnalysis[1]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[1] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[1]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[1]]}}</p>
            </div>
        </div>
        <v-divider/>
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[1]">
                    <p>{{name[1]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[2]" class="typeImg">
                <p>{{types[typeAnalysis[2]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[2]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[2]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[3] != 'x'">
                <img :src="typeImg[3]" class="typeImg">
                <p>{{types[typeAnalysis[3]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[3] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[3]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[3]]}}</p>
            </div>
        </div>
        <v-divider/>
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[2]">
                    <p>{{name[2]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[4]" class="typeImg">
                <p>{{types[typeAnalysis[4]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[4]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[4]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[5] != 'x'">
                <img :src="typeImg[5]" class="typeImg">
                <p>{{types[typeAnalysis[5]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[5] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[5]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[5]]}}</p>
            </div>
        </div>
        <v-divider/>
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[3]">
                    <p>{{name[3]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[6]" class="typeImg">
                <p>{{types[typeAnalysis[6]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[6]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[6]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[7] != 'x'">
                <img :src="typeImg[7]" class="typeImg">
                <p>{{types[typeAnalysis[7]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[7] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[7]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[7]]}}</p>
            </div>
        </div>
        <v-divider/>
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[4]">
                    <p>{{name[4]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[8]" class="typeImg">
                <p>{{types[typeAnalysis[8]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[8]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[8]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[9] != 'x'">
                <img :src="typeImg[9]" class="typeImg">
                <p>{{types[typeAnalysis[9]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[9] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[9]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[9]]}}</p>
            </div>
        </div>
        <v-divider/>
        <div class="pkContainer">
            <div class="innerContainer3">
                <div>
                    <img :src="sprite[5]">
                    <p>{{name[5]}}</p>
                </div>
                <v-divider vertical />
            </div>
            <div class="innerContainer">
                <img :src="typeImg[10]" class="typeImg">
                <p>{{types[typeAnalysis[10]].name}}</p>
            </div>
            <div class="innerContainer2">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[10]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[10]]}}</p>
            </div>
            <div class="innerContainer" v-if="typeAnalysis[11] != 'x'">
                <img :src="typeImg[11]" class="typeImg">
                <p>{{types[typeAnalysis[11]].name}}</p>
            </div>
            <div class="innerContainer2" v-if="typeAnalysis[11] != 'x'">
                <p>Deals Double Damage To: {{strongCount[typeAnalysis[11]]}}</p>
                <p>Takes Double Damage From: {{weakCount[typeAnalysis[11]]}}</p>
            </div>
        </div>
    </div>
</div>
</template>


<script>
import { types } from '../assets/type.js'

export default {
  data: () => ({
      typeObject: null,
      types: types
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
                        typeArray.push(17);
                    };
                }
            }
          return typeArray;
      },
      weakCount() {
          let weakArray = ["fighting", "flying, psychic, fairy", "rock, electric, ice", "ground", "water, grass, ice", "fighting, ground, steel, water, grass", "flying, rock, fire", "ghost, dark", "fighting, ground, fire", "ground, rock, water", "grass, electric", "flying, poison, bug, fire, ice", "ground", "bug, ghost, dark", "fighting, rock, steel, fire", "ice, dragon, fairy", "fighting, bug, fairy", "poison, steel"];
          
          return weakArray;
      },
      strongCount() {
          let strongArray = ["none", "normal, rock, steel, ice, dark", "fighting, bug, grass", "grass, fairy", "poison, rock, steel, fire, electric", "flying, bug, fire, ice", "grass, psychic, dark", "ghost, psychic", "rock, ice, fairy", "bug, steel, grass, ice", "ground, rock, fire", "ground, rock, water", "flying, water", "fighting, poison", "flying, ground, grass, dragon", "dragon", "ghost, psychic", "fighting, dragon, dark"];
          return strongArray;
      },
      typeImg() {
          let imgArray = [];
          let srcArray = ['https://vignette.wikia.nocookie.net/pokemongo/images/f/fb/Normal.png/revision/latest/scale-to-width-down/64?cb=20161013132914', 'https://vignette.wikia.nocookie.net/pokemongo/images/3/30/Fighting.png/revision/latest/scale-to-width-down/64?cb=20161013132827',
        'https://vignette.wikia.nocookie.net/pokemongo/images/7/7f/Flying.png/revision/latest/scale-to-width-down/64?cb=20161013132839', 'https://vignette.wikia.nocookie.net/pokemongo/images/0/05/Poison.png/revision/latest/scale-to-width-down/64?cb=20161013133014', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/8/8f/Ground.png/revision/latest/scale-to-width-down/64?cb=20161013132902', 'https://vignette.wikia.nocookie.net/pokemongo/images/0/0b/Rock.png/revision/latest/scale-to-width-down/64?cb=20161013133022', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/7/7d/Bug.png/revision/latest/scale-to-width-down/64?cb=20161013132753', 'https://vignette.wikia.nocookie.net/pokemongo/images/a/ab/Ghost.png/revision/latest/scale-to-width-down/64?cb=20161013132847', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/c/c9/Steel.png/revision/latest/scale-to-width-down/64?cb=20161013133029', 'https://vignette.wikia.nocookie.net/pokemongo/images/3/30/Fire.png/revision/latest/scale-to-width-down/64?cb=20161013132833', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/9/9d/Water.png/revision/latest/scale-to-width-down/64?cb=20161013133222', 'https://vignette.wikia.nocookie.net/pokemongo/images/c/c5/Grass.png/revision/latest/scale-to-width-down/64?cb=20161013132855', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/2/2f/Electric.png/revision/latest/scale-to-width-down/64?cb=20161013132813', 'https://vignette.wikia.nocookie.net/pokemongo/images/2/21/Psychic.png/revision/latest/scale-to-width-down/64?cb=20161013133006', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/7/77/Ice.png/revision/latest/scale-to-width-down/64?cb=20161013132908', 'https://vignette.wikia.nocookie.net/pokemongo/images/c/c7/Dragon.png/revision/latest/scale-to-width-down/64?cb=20161013132807', 
        'https://vignette.wikia.nocookie.net/pokemongo/images/0/0e/Dark.png/revision/latest/scale-to-width-down/64?cb=20161013132800', 'https://vignette.wikia.nocookie.net/pokemongo/images/4/43/Fairy.png/revision/latest/scale-to-width-down/64?cb=20161013132820']
          for (let i = 0; i < this.typeAnalysis.length; i++) {
              if(this.typeAnalysis[i] != 'x') {
                let imgNum = srcArray[this.typeAnalysis[i]];
                imgArray.push(imgNum);
              } else {
                imgArray.push('x');
              };
            }
          return imgArray;
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
    width: 150px;
    margin-bottom: -40px;
}
.pkBtn {
    background-color: red;
}
p {
    text-align: center;
    width: 100%;
    margin-top: 15px;
}
.pkContainer {
    display: flex; 
    justify-content: space-between;
    width: 100%;
}
.innerContainer {
    text-align: center;
}
.innerContainer2 {
    text-align: center;
    background-color: rgb(233, 233, 233);
    width: 28%;
}
.innerContainer3 {
    display: flex;
}
.typeImg {
    height: 80px;
    width: 80px;
    margin-top: 30px;
    margin-bottom: -2px;
}
</style>



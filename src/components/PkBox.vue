<template>
<div id="dex-box" style="height: 450px; overflow: scroll;">
    <p>Click on a Pokémon to Learn More</p><br>
    <div v-for="pkmon in pkmon" :key="pkmon.name" >
    <pk-comp :pkmon="pkmon"></pk-comp>
    </div>
</div>
</template>

<script>
import PkComp from './PkComp';

export default {
  props: ["pkmon"],
  components: {
      PkComp
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
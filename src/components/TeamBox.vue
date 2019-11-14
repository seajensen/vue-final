<template>
<div id="dex-box">
    <p>Click on a Pokémon to Learn More</p><br>
    <div id="TeamDisplay">
        <p>Name: {{ name[0] }}, {{ name[1] }}, {{ name[2] }}, {{ name[3] }}</p>
    </div>
</div>
</template>


<script>
import PkComp from './PkComp';

export default {
  computed: {
      name() {
          return this.$store.state.teamName;
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



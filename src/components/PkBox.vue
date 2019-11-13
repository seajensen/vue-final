<template>
<div id="dex-box">
    <div v-for="pkmon in pkmon" :key="pkmon.name">
    <pk-comp :pkmon="pkmon"></pk-comp>
    </div>
    <p> 1 | 2 | 3 | 4 | 5 | 6 </p>
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
    width: 500px;
    padding-bottom: 15px;
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
</style>



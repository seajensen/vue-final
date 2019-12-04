<template>
<div id="dex-box">
    <div style="display: flex">
        <img :src="sprite[0]"><p>{{name[0]}}</p>
        <p>{{typeObject}}</p>
    </div>
</div>
</template>


<script>
export default {
  data: () => ({
      typeObject: null
  }),
  computed: {
      type() {
          return this.$store.state.teamType;
      },
      name() {
          return this.$store.state.teamName;
      },
      sprite() {
          return this.$store.state.teamSprite;
      }
  },
  mounted () {
      this.$axios.get('https://pokeapi.co/api/v2/type/1/').then
            (response => {
              this.typeObject = response.data.results
          })
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



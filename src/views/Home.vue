<template>
  <div class="home">
    <layout :pkmon="pkmon"/>
  </div>
</template>

<script>
// @ is an alias to /src
import layout from '../components/Layout';
import { pkmon } from '../assets/pkmon.js'

export default {
  name: 'home',
  components: {
    layout,
  },
  data: () => {
    return {
      pkmon: pkmon,
    }
  },
}
</script>

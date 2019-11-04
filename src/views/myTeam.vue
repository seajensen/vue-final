<template>
  <div class="about">
    <team-layout :pkmon="pkmon"/>
  </div>
</template>

<script>
// @ is an alias to /src
import teamLayout from '../components/TeamLayout';
import { pkmon } from '../assets/pkmon.js'

export default {
  name: 'home',
  components: {
    teamLayout,
  },
  data: () => {
    return {
      pkmon: pkmon,
    }
  },
}
</script>
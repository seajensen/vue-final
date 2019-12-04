<template>
  <div class="about">
    <type-layout :pkmon="pkmon"/>
  </div>
</template>

<script>
// @ is an alias to /src
import typeLayout from '../components/TypeLayout';

export default {
  name: 'home',
  components: {
    typeLayout,
  },
  data: () => {
    return {
      pkmon: pkmon,
    }
  },
}
</script>
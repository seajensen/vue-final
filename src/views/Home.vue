<template>
  <div class="home">
    <Pkdex msg="Hiragana"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Pkdex from '@/components/Pkdex.vue'

export default {
  name: 'home',
  components: {
    Pkdex
  }
}
</script>

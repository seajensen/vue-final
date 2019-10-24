<template>
  <div class="home">
    <Hiragana msg="Hiragana"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Hiragana from '@/components/Hiragana.vue'

export default {
  name: 'home',
  components: {
    Hiragana
  }
}
</script>

<template>
  <div class="about">
    <saved-layout/>
  </div>
</template>

<script>
// @ is an alias to /src
import savedLayout from '../components/SavedLayout';

export default {
  name: 'home',
  components: {
    savedLayout,
  },
  data: () => {
    return {
        
    }
  },
}
</script>
<template>
  <div class="home">
    <AppMain msg="Tchau mundo"/>
  </div>
</template>

<script>
// @ is an alias to /src
import AppMain from '@/components/AppMain.vue'

export default {
  name: 'Home',
  components: {
    AppMain
  }
}
</script>

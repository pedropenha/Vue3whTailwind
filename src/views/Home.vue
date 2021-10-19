<template>
  <div class="home">
    <AppMain msg="oi world"/>
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

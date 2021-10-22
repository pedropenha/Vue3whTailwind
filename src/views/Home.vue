<template>
  <div class="home">
    <NavBar/>
    <Carrousel/>
    <router-link to="/about"/>
<!--    <AppMain msg="Tchau mundo"/>-->
  </div>
</template>

<script>
// @ is an alias to /src
// import AppMain from '@/components/AppMain.vue'
import NavBar from '../components/NavBar'
import Carrousel from '../components/carrousel'
export default {
  name: 'Home',
  components: {
    Carrousel,
    // AppMain,
    NavBar
  }
}
</script>

<template>
  <nav id="demo">
    <transition-group name="slide-fade">
      <div v-if="!this.bb" class="wrapper">
        <div class="image-logo">
          <img class="image" src="@/assets/img/logo.jpg"/>
        </div>
        <div class="btn-bb">
          <BB v-on:click="isClick(this.bb)"/>
        </div>
      </div>

      <div style="width: 100%; height: 100%; background-color: black" v-if="this.bb">
        <button v-on:click="isClick(this.bb)" style="color: #42b983">X</button>
      </div>
    </transition-group>
  </nav>
</template>

<script>
import BB from './buttonBurguer'
export default {
  name: 'NavBar',
  components: {
    BB
  },
  data () {
    return {
      bb: false
    }
  },
  methods: {
    isClick (bb) {
      this.bb = !this.bb
    }
  }
}
</script>

<style lang="scss" scoped>
.wrapper{
  @apply flex bg-emerald-600 w-full items-center justify-between sm:h-10 lg:justify-start;
  height: 20vh;
}
.btn-bb{
  @apply -mr-2 flex items-center md:hidden
}
.image-logo{
  @apply h-full;
  width: 10%;
  //padding: 5%;
}
.image{
  @apply w-full h-auto rounded-full
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
  /* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}
</style>

<template>
  <div class="flex justify-center items-center h-screen">
    <h1 class="font-bold text-9xl text-emerald-500 text-center">{{msg}}</h1>
  </div>
</template>

<script>
export default {
  name: 'AppMain',
  props: {
    msg: String
  }
}
</script>

<style lang="scss" scoped>

</style>

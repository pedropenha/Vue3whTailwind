<template>
  <section id="about">
    <div class="main">
      <p>Ola mundo</p>
    </div>
    <p>Tchau mundo</p>
  </section>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style lang="scss" scoped>
#about{
  .main{
    @apply flex justify-between items-center;
    width: 100%;
    height: 100%;
    p{
      @apply text-emerald-500;
    }
  }
}
</style>

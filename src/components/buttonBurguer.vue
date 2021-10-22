<template>
  <button type="button" class="btn" aria-expanded="false">
    <span >Open main menu</span>

    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
    </svg>
  </button>
</template>
<script>
export default {
  name: 'BB'
}
</script>

<style lang="scss" scoped>
  .btn{
    @apply bg-orange-600 rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:text-gray-500
    hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500;
    span{
      @apply sr-only;
    }
    svg{
      @apply h-6 w-6;
    }
  }

</style>

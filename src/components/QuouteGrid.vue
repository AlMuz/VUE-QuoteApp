<template>
  <div class="row">
    <appQuote v-for="quote in quotes">{{ quote }}</appQuote>
  </div>
</template>

<script>
  import Quoute from './Quoute.vue'

  export default {
    props: ['quotes'],
    components: {
      appQuote: Quoute
    }
  }
</script>

<style>
</style>

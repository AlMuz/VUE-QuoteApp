<template>
  <div class="container">
    <appQuoteGrid :quotes="quotes">
    </appQuoteGrid>
  </div>
</template>

<script>
  import QuouteGrid from './components/QuouteGrid.vue'

  export default {
    data: function() {
      return {
        quotes: [
          'Just a quoute to see smth'
        ],
        maxQuoutes: 10
      }
    },
    components: {
      appQuoteGrid: QuouteGrid
    }
  }
</script>

<style>
</style>

<template>
  <div class="container">
    <appNewQuote @quoteAdded="newQuote"></appNewQuote>
    <appQuoteGrid :quotes="quotes"></appQuoteGrid>
  </div>
</template>

<script>
  import QuouteGrid from './components/QuouteGrid.vue'
  import NewQuote from './components/NewQuote.vue'

  export default {
    data: function() {
      return {
        quotes: [
          'Just a quoute to see smth'
        ],
        maxQuoutes: 10
      }
    },
    methods: {
      newQuote(quote) {
        this.quotes.push(quote);
      }
    },
    components: {
      appQuoteGrid: QuouteGrid,
      appNewQuote: NewQuote,
    }
  }
</script>

<style>
</style>

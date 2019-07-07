<template>
  <div class="container">
    <appNewQuote @quoteAdded="newQuote"></appNewQuote>
    <appQuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></appQuoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          INFO: Click on quote to delete it!
        </div>
      </div>
    </div>
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
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1);
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

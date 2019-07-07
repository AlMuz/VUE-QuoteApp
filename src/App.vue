<template>
  <div class="container">
    <appHeader :quoteCount="quotes.length" :maxCounts="maxQuotes"></appHeader>
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
  import Header from './components/Header.vue'

  export default {
    data: function() {
      return {
        quotes: [
          'Just a quoute to see smth'
        ],
        maxQuotes: 10
      }
    },
    methods: {
      newQuote(quote) {
        if(this.quotes.length >= this.maxQuotes) {
          return alert('Please delete quotes first');
        }
        this.quotes.push(quote);
      },
      deleteQuote(index) {
        this.quotes.splice(index, 1);
      }
    },
    components: {
      appQuoteGrid: QuouteGrid,
      appNewQuote: NewQuote,
      appHeader: Header,
    }
  }
</script>

<style>
</style>

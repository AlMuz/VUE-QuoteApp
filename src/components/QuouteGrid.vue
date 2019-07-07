<template>
  <div class="row">
    <appQuote v-for="(quote, index) in quotes" @click.native="deleteQuote(index)">{{ quote }}</appQuote>
  </div>
</template>

<script>
  import Quoute from './Quoute.vue'

  export default {
    props: ['quotes'],
    components: {
      appQuote: Quoute
    },
    methods: {
      deleteQuote(index) {
        this.$emit('quoteDeleted', index);
      }
    }
  }
</script>

<style>
</style>

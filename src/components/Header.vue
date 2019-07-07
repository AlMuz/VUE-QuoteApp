<template>
  <div>
    <h3>Quotes added</h3>
    <div class="col-sm-12">
      <div class="progress">
        <div class="progress">
          <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100"
            :style="{width: (quoteCount/maxCounts) * 100 + '%'}">
            {{ quoteCount }} /  {{ maxCounts }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['quoteCount', 'maxCounts']
  }
</script>

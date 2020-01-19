<template>
  <div class="container">
    <app-quoteGrid :quotes="quotes"></app-quoteGrid>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";

export default {
  data: function() {
    return {
      quotes: ["This is the first quote"],
      maxQuotes: 10
    };
  },
  components: {
    appQuoteGrid: QuoteGrid
  }
};
</script>

<style></style>

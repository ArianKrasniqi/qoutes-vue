<template>
  <div class="container">
    <app-newQuote @quoteAdded="newQuote($event)"></app-newQuote>
    <app-quoteGrid :quotes="quotes"></app-quoteGrid>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">Click on Qoute to delete it!</div>
      </div>
    </div>
  </div>
</template>

<script>
import QuoteGrid from "./components/QuoteGrid.vue";
import NewQuote from "./components/NewQuote.vue";

export default {
  data: function() {
    return {
      quotes: ["This is the first quote"],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      console.log(quote);
      this.quotes.push(quote);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  }
};
</script>

<style></style>

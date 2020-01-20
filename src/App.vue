<template>
  <div class="container">
    <app-progress
      :quoteCount="quotes.length"
      :maxQuotes="maxQuotes"
    ></app-progress>
    <app-newQuote @quoteAdded="newQuote($event)"></app-newQuote>
    <app-quoteGrid
      :quotes="quotes"
      @quoteDeleted="deleteQoute($event)"
    ></app-quoteGrid>
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
import Progress from "./components/Progress.vue";

export default {
  data: function() {
    return {
      quotes: ["This is the first quote"],
      maxQuotes: 10
    };
  },
  methods: {
    newQuote(quote) {
      if (this.quotes.length == 10) {
        return alert("Please delete a quote first!");
      }
      this.quotes.push(quote);
    },
    deleteQoute(index) {
      this.quotes.splice(index, 1);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appProgress: Progress
  }
};
</script>

<style></style>

<template>
  <div class="row">
    <hr />
    <app-quote v-for="quote in quotes">
      <h3>{{ quote }}</h3>
    </app-quote>
  </div>
</template>
<script>
import Quote from "./Quote.vue";

export default {
  props: ["quotes"],
  components: {
    appQuote: Quote
  }
};
</script>

<style></style>

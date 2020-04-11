<template>
  <div>
  <v-progress-linear :value="quotesSize * 10" height="25">
      <strong> {{ quotesSize }}/10</strong>
    </v-progress-linear>
  </div>
</template>

<script>
export default {
  props: {
    getQuotes: Function
  },
  computed: {
    quotesSize: function() {
      return this.getQuotes().length;
    }
  }
};
</script>

<style></style>

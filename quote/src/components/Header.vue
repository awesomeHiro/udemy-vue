<template>
  <div>
  <v-progress-linear :value="getQuotes().length * 10" height="25">
      <strong> {{ getQuotes().length }}/10</strong>
    </v-progress-linear>
  </div>
</template>

<script>
export default {
  props: {
    getQuotes: Function
  },
};
</script>

<style></style>

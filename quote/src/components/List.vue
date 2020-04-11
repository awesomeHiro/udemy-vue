<template>
  <div class="container">
    <h1>list</h1>
    <ul id="example-1">
      <li v-for="quote in quotes" :key="quote">
        {{ quote }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    getQuotes: Function
  },
  computed:{
      quotes: function () {
          return this.getQuotes()
      }
  }
};
</script>

<style></style>

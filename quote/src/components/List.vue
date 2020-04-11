<template>
  <div class="container">
    <h1>list</h1>
    <ul id="example-1">
      <li v-for="quote in getQuotes()" :key="quote">
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
};
</script>

<style></style>

<template>
  <div class="component">
    <h3>Details</h3>
    <p>name: {{ name }}</p>
    <p>age: {{ age }}</p>
  </div>
</template>

<script>
export default {
  props: {
    name: {},
    age: {},
  },
};
</script>

<style scoped>
div {
  background-color: lightcoral;
}
</style>

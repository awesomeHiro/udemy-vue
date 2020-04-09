<template>
  <div class="component">
    <h3>Details</h3>
    <p>name: {{ name }}</p>
    <p>age: {{ age }}</p>
    <button @click="reverseName">reverseName</button>
    <button @click="defaultName">defaultName</button>
    <button @click="resetName">resetName</button>
  </div>
</template>

<script>
export default {
  props: {
    name: {},
    age: {},
    resetName: Function
  },
  methods: {
    reverseName() {
      this.name = this.name.split("").reverse().join("");
      this.$emit("nameChanged", this.name);
    },
    defaultName() {
      this.name = "max";
    },
  },
};
</script>

<style scoped>
div {
  background-color: lightcoral;
}
</style>

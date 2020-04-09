<template>
  <div class="component">
    <h3>Edit</h3>
    <button @click="reverseName">reverseName</button>
    <button @click="resetName">resetName</button>\
    <hr>
    <button @click="editAge">EditAge</button>
  </div>
</template>

<script>
  export default{
    props:{
      reverseName: Function,
      resetName: Function,
      editAge: Function
    },
    methods:{
    }
  }
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>

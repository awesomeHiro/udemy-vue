<template>
  <div class="component">
    <h3>Edit</h3>
    <p>name: {{ name }}</p>
    <p>age: {{ age }}</p>
    <button @click="editAge">EditAge</button>
  </div>
</template>

<script>
  export default{
    props:{
      name:{},
      age:{}
    },
    methods:{
      editAge(){
        this.age = 30
        this.$emit('ageChanged', this.age)
      }
    }
  }
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>

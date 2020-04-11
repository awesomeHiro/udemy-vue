<template>
  <div class="container">
    <v-form ref="form" v-model="valid" :lazy-validation="lazy">
      <v-text-field
        v-model="newQuote"
        required
      ></v-text-field>

      <v-btn color="success" @click="add()">
        Add Quote
      </v-btn>
    </v-form>
    {{newQuote}}
  </div>
</template>

<script>
export default {
  props: {
    addQuote: Function
  },

  data: () => ({
    newQuote: '',
    isEmpty: false
  }),
    methods: {
        add(){
            this.addQuote(this.newQuote)
        }
    }
};
</script>

<style></style>

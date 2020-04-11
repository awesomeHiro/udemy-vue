<template>
  <div class="container">
    <v-form ref="form">
      <v-text-field
        v-model="newQuote"
        required
      ></v-text-field>
      <v-btn color="success" @click="add()">
        Add Quote
      </v-btn>
    </v-form>
  </div>
</template>

<script>
export default {
  props: {
    addQuote: Function
  },

  data: () => ({
    newQuote: '',
  }),
    methods: {
        add(){
            this.addQuote(this.newQuote)
            this.$refs.form.reset()
        }
    }
};
</script>

<style></style>

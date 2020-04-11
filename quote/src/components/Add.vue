<template>
  <div class="container">
    <v-form ref="form">
      <v-text-field
        v-model="newQuote"
        placeholder="edit me"
        required
        v-on:keydown.enter.prevent='add'
        :disabled="quotesSize >= 10"
      ></v-text-field>
      <v-btn :disabled="quotesSize >= 10 || !this.newQuote" color="success" @click="add()">
        Add Quote
      </v-btn>
    </v-form>
  </div>
</template>

<script>
export default {
  props: {
    addQuote: Function,
    getQuotes: Function
  },

  data: () => ({
    newQuote: '',
  }),
    computed:{
      quotesSize: function () {
          return this.getQuotes().length
      }
  },

    methods: {
        add(){
            if (this.quotesSize >= 10) return
            if (!this.newQuote) return
            this.addQuote(this.newQuote)
            this.$refs.form.reset()
        }
    }
};
</script>

<style></style>

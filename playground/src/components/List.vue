<template>
  <div class="container">
    <v-container fluid>
      <v-card v-for="(quote, index) in getQuotes()" :key="quote">
        <v-row>
          <v-col> <v-card-title v-text="quote"></v-card-title> </v-col>
          <v-col cols="auto">
            <v-card-actions>
              <v-btn icon @click="deleteQuote(index)">
                <v-icon>mdi-delete</v-icon>
              </v-btn>
            </v-card-actions>
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  props: {
    getQuotes: Function,
    deleteQuote: Function
  }
};
</script>

<style></style>

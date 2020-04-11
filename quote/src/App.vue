<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Quote</h1>
      <v-spacer></v-spacer>
      <h1>Awesome</h1>
    </v-app-bar>

    <v-content>
      <v-container fluid fill-wide>
        <Header />
        <v-divider></v-divider>
        <Add />
        <v-divider></v-divider>
        <List :getQuotes="getQuotes" />
        <v-divider></v-divider>
        <Footer />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Add from "./components/Add";
import List from "./components/List";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    Header,
    Add,
    List,
    Footer
  },

  data: () => ({
    quotes: [
      "Quote1",
      "Quote2",
      "Quote3",
      "Quote4",
      "Quote5",
      "Quote6",
      "Quote7",
      "Quote8",
      "Quote9",
      "Quote10"
    ]
  }),
  methods:{
    getQuotes(){
      return this.quotes
    },
    // addQuote(){
      
    // }
  }
};
</script>

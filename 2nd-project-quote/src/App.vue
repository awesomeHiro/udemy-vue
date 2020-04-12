<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <h1>Quote</h1>
      <v-spacer></v-spacer>
      <h1>Awesome</h1>
    </v-app-bar>

    <v-content>
      <v-container fluid fill-wide>
        <Header :getQuotes="getQuotes" />
        <Add :getQuotes="getQuotes" :addQuote="addQuote" />
        <List :getQuotes="getQuotes" :deleteQuote="deleteQuote" />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
import Header from "./components/Header";
import Add from "./components/Add";
import List from "./components/List";

export default {
  name: "App",

  components: {
    Header,
    Add,
    List
  },

  data: () => ({
    quotes: [
      "The greatest glory in living lies not in never falling, but in rising every time we fall. -Nelson Mandela",
      "The way to get started is to quit talking and begin doing. -Walt Disney",
      "Your time is limited, so don't waste it living someone else's life. Don't be trapped by dogma – which is living with the results of other people's thinking. -Steve Jobs",
      "If life were predictable it would cease to be life, and be without flavor. -Eleanor Roosevelt",
      "If you look at what you have in life, you'll always have more. If you look at what you don't have in life, you'll never have enough. -Oprah Winfrey",
      "If you set your goals ridiculously high and it's a failure, you will fail above everyone else's success. -James Cameron",
      "Life is what happens when you're busy making other plans. -John Lennon"
    ]
  }),
  methods: {
    getQuotes() {
      return this.quotes;
    },
    addQuote(newQuote) {
      this.quotes.unshift(newQuote);
    },
    deleteQuote(index){
      this.quotes.splice(index, 1,);
    }
  }
};
</script>

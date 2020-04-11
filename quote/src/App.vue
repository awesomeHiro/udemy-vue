<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <h1>Quote</h1>
      <v-spacer></v-spacer>
      <h1>Awesome</h1>
    </v-app-bar>

    <v-content>
      <Header/>
      <v-divider></v-divider>
      <Add/>
  <v-divider></v-divider>
      <List/>
  <v-divider></v-divider>
      <Footer/>
    </v-content>
  </v-app>
</template>

<script>
import Header from './components/Header';
import Add from './components/Add';
import List from './components/List';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Header,
    Add,
    List,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>

<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-container>
        <v-row justify="center" align="center" class="navbar_main">
          POOL JOLIETTE ET CIE
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    HelloWorld,
    Footer,
  },

  data: () => ({
    //
  }),
};
</script>
<template>
  <v-app>
    <app-header />

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
// import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    // HelloWorld,
    AppHeader,
  },

  data: () => ({
    //
  }),
};
</script>

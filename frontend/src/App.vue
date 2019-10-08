<template>
  <v-app>
    <v-content>
      <Navigation/>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Navigation from "./components/Navigation";

export default {
  name: "App",
  components: {
    HelloWorld,
    Navigation,
  },
};
</script>

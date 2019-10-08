<template>
  <v-app id="sandbox">
    <v-navigation-drawer
      v-model="primaryDrawer.model"
      :clipped="primaryDrawer.clipped"
      :permanent="primaryDrawer.type === 'permanent'"
      :temporary="primaryDrawer.type === 'temporary'"
      app
      overflow
    ></v-navigation-drawer>
    <v-app-bar :clipped-left="primaryDrawer.clipped" app>
      <v-app-bar-nav-icon v-if="primaryDrawer.type !== 'permanent'" v-on:click.stop="primaryDrawer.model = !primaryDrawer.model"></v-app-bar-nav-icon>
      <v-toolbar-title style="width:100%;margin-top:20px;">
        <span>KinWorld</span>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link to="/homepage">hompage</router-link>
        <v-switch v-model="$vuetify.theme.dark" primary label="Dark" style="float:right"></v-switch>
      </v-toolbar-title>
    </v-app-bar>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawers: ["Default (no property)"],
    primaryDrawer: {
      model: null,
      type: "default (no property)",
      clipped: false,
    },
    footer: {
      inset: true
    }
  })
};
</script>

<template>
  <v-app>
    <v-app-bar class="grey lighten-5" height="74" app>
      <img class="mx-2" src="./assets/logo.svg" style="height: 65px" />
      <span
        class="text-truncate text-h4 blue-grey--text darken-1"
        style="font-family: Poppins"
        >A Dog With a Mission</span
      >
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-navigation-drawer
      permanent
      expand-on-hover
      height="300"
      width="56px"
      id="fixed"
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="./assets/logo.svg"></v-img>
          </v-list-item-avatar>
        </v-list-item>

        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title class="text-h6">
              Sandra Adams
            </v-list-item-title>
            <v-list-item-subtitle>sandra_a88@gmail.com</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list nav dense>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-folder</v-icon>
          </v-list-item-icon>
          <v-list-item-title>My Files</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-account-multiple</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Shared with me</v-list-item-title>
        </v-list-item>
        <v-list-item link>
          <v-list-item-icon>
            <v-icon>mdi-star</v-icon>
          </v-list-item-icon>
          <v-list-item-title>Starred</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <router-view to="/"></router-view>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: false,
    routes: [
      { name: "Home", route: "/" },
      { name: "About", route: "/about" },
      { name: "Products", route: "/products" },
      { name: "Team", route: "/team" },
    ],
  }),
};
</script>

<style>
a:not(.v-btn--active) {
  color: #2196f3 !important;
  background: white !important;
}

#fixed {
  position: absolute !important;
  top: 50% !important;
  left: 0;
  transform: translateY(-50%) !important;
}
</style>
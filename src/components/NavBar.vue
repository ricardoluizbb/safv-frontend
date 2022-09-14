<template>
  <v-container fluid>
    <nav>
      <v-toolbar class="primary" app>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title class="pa-0 ml-4">
          <span style="color: white">SAFV</span>
        </v-toolbar-title>

        <v-divider
          class="ml-8"
          style="background-color: white"
          vertical
        ></v-divider>
        <v-spacer />

        <v-btn
          style="color: white"
          outlined
          flat
          @click="$router.push({ path: '/' })"
        >
          <span>Sair</span>
          <v-icon right>mdi-logout</v-icon>
        </v-btn>
      </v-toolbar>
      <v-navigation-drawer
        v-model="drawer"
        class="secondary"
        app
        temporary
      ></v-navigation-drawer>
    </nav>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
  }),
};
</script>
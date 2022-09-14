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
      <v-navigation-drawer v-model="drawer" class="secondary" app temporary>
        <v-list nav class="mt-8">
          <v-list-item
            style="color: white"
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon style="color: white">{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </nav>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    items: [
      { title: "Veículos", icon: "mdi-truck-outline" },
      { title: "Usuários", icon: "mdi-account-group" },
      { title: "Motoristas", icon: "mdi-account-tie-hat" },
      { title: "Relatórios", icon: "mdi-book-open-outline" },
      { title: "Diário de bordo", icon: "mdi-notebook-edit-outline" },
    ],
    right: null,
  }),
};
</script>
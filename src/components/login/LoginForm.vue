<template>
  <v-app>
    <v-container style="height: 100%; background-color: F5F5F5" fluid>
      <v-layout align-center justify-center>
        <v-flex class="mt-10" xs12 sm8 md4>
          <div class="mt-8">
            <v-img
              src="@/assets/logo.svg"
              transition="scale-transition"
              height="100%"
              width="100%"
            />
          </div>
          <v-card class="elevation-12">
            <v-toolbar dark color="primary">
              <v-toolbar-title style="text-align: center"
                >Sistema Administrativo de Frota Veicular</v-toolbar-title
              >
            </v-toolbar>
            <v-card-text>
              <form ref="form" @submit.prevent="login()">
                <v-text-field
                  append-icon="mdi-account-circle-outline"
                  v-model="username"
                  name="username"
                  label="Usuário"
                  type="text"
                  placeholder="username"
                  required
                  outlined
                ></v-text-field>

                <v-text-field
                  append-icon="mdi-lock-outline"
                  v-model="password"
                  name="password"
                  label="Senha"
                  type="password"
                  placeholder="password"
                  required
                  outlined
                ></v-text-field>
                <v-btn type="submit" class="mt-4" color="primary" value="log in"
                  >Login</v-btn
                >
              </form>
            </v-card-text>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "LoginForm",
  data() {
    return {
      username: "",
      password: "",
    };
  },
  methods: {
    login() {
      const { username } = this;
      console.log(username + "logged in");
      this.$router.push({ name: "home" });
    },
  },
};
</script>
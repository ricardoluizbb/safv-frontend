<template>
  <v-app>
    <nav-bar />
    <v-container
      class="fill-height"
      style="width: 100%; background-color: #c4c4c4"
    >
      <register-vehicle />
    </v-container>
  </v-app>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import RegisterVehicle from "@/components/vehicle/RegisteVehicle.vue";
export default {
  name: "LoginView",

  components: {
    NavBar,
    RegisterVehicle,
  },
};
</script>
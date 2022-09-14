<template>
  <v-container style="height: 100%">
    <v-container style="height: 100%; width: 900px">
      <v-card height="100%">
        <v-card-title
          style="font-size: 30px"
          class="d-flex flex-column align-center mb-8"
        >
          Cadastro de Veículos
        </v-card-title>
        <form>
          <v-card-actions class="d-flex flex-column">
            <v-col class="d-inline-flex" cols="12">
              <v-text-field class="mx-2" label="Placa" outlined></v-text-field>
              <v-text-field
                class="mx-2"
                label="Fabricante"
                outlined
              ></v-text-field>
              <v-text-field class="mx-2" label="Cor" outlined></v-text-field>
              <v-text-field class="mx-2" label="Ano" outlined></v-text-field>
            </v-col>

            <v-col class="d-inline-flex" cols="12">
              <v-text-field class="mx-2" label="Placa" outlined></v-text-field>
              <v-select
                :items="items"
                label="Outlined style"
                outlined
              ></v-select>
            </v-col>
          </v-card-actions>
        </form>
      </v-card>
    </v-container>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    items: ["Foo", "Bar", "Fizz", "Buzz"],
  }),
};
</script>
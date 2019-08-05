<template>
  <v-container>
    <v-layout pa-5 text-center wrap>
      <v-flex md6 ma-2>

        <v-card dark color="primary" class="mx-auto" outlined elevation="5">
          <v-img class="white--text" height="200px" :src="require('../assets/motor_home_1.jpg')">
            <v-card-title class="align-end fill-height">Registrar vehículo</v-card-title>
          </v-img>
          <v-card-text>Registre la entrada de vehículos</v-card-text>
          <v-card-actions>
            <v-btn  v-show="false"></v-btn>
            <v-spacer></v-spacer>
            <v-btn :to="'register'" outlined>Empezar</v-btn>
          </v-card-actions>
        </v-card>

      </v-flex>

      <v-flex md6 ma-2>
        <v-card dark color="cyan" class="mx-auto" outlined elevation="5">
          <v-img class="white--text" height="200px" :src="require('../assets/taller.jpg')">
            <v-card-title class="align-end fill-height">Consultar estado de servicio</v-card-title>
          </v-img>
          <v-card-text>Consulte  estado de servicio</v-card-text>
          <v-card-actions>
            <v-btn  v-show="false"></v-btn>
            <v-spacer></v-spacer>
            <v-btn :to="'register'" outlined>Empezar</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>

       <v-flex md6 ma-2>
        <v-card dark class="mx-auto" outlined elevation="5">
          <v-img class="white--text" height="200px" :src="require('../assets/revolt.jpg')">
            <v-card-title class="align-end fill-height">Administrar mis talleres</v-card-title>
          </v-img>
          <v-card-text>Administre usuarios, productos y servicios</v-card-text>
          <v-card-actions>
            <v-btn  v-show="false"></v-btn>
            <v-spacer></v-spacer>
            <v-btn :to="'register'" outlined>Empezar</v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>

    </v-layout>
  </v-container>
</template>

<script>
export default {
  components: {}
};
</script>

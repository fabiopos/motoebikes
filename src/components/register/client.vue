<template>
  <v-form ref="form" v-model="valid">
    <v-divider></v-divider>

    <v-layout pa-1 wrap text-left>

      <v-flex xs12 sm12 md3>
        <v-card class="pa-5 ma-2" elevation="12">          
          <v-text-field append-icon="person" v-model="name" :counter="10" label="Nombres" required></v-text-field>
          <v-text-field append-icon="person" v-model="lastName" :counter="10" label="Apellidos" required></v-text-field>
          <v-text-field append-icon="email" v-model="email" label="E-mail" required></v-text-field>
        </v-card>
      </v-flex>
      

      <v-flex xs12 sm12 md3 offset-sm1 >
        <v-card class="pa-5 ma-2" elevation="12">        
          <v-select append-icon="assignment_ind" v-model="idType" :items="idTypes" label="Tipo de documento" required></v-select>
          <v-text-field type="number" append-icon="assignment_ind" v-model="identification" :counter="10" label="Número de documento" required></v-text-field>
          <v-text-field append-icon="assignment_ind" v-model="city" :counter="10" label="Ciudad de residencia" required></v-text-field>
        </v-card>

      </v-flex>
      <v-flex xs12 md3 offset-sm1>
        <v-card class="pa-5 ma-2" elevation="12">        
          <v-text-field append-icon="place" v-model="address" label="Dirección"></v-text-field>
          <v-text-field append-icon="phone" type="number" v-model="phone" label="Teléfono fijo" ></v-text-field>
          <v-text-field append-icon="phone" type="number" v-model="cellphone" label="Teléfono celular" ></v-text-field>
        </v-card>
      </v-flex>
      
    </v-layout>
    
  </v-form>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    name: "",
    lastName: "",
    address: "",
    identification: "",
    idType: "",
    idTypes: [
      "Cédula de Ciudadanía",
      "Cédula de extranjería",
      "Pasaporte",
      "NIT"
    ],
    city: "",
    email: "",
    phone: "",
    cellphone: ""
  })
};
</script>

<style>
</style>

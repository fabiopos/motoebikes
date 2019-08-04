<template>
  <v-form ref="form" v-model="valid">
    <v-divider></v-divider>

    <v-layout pa-1 wrap text-left>

      <v-flex xs12 sm12 md3>
         <v-icon>person</v-icon>
        <v-text-field v-model="name" :counter="10" label="Nombres" required></v-text-field>
        <v-text-field v-model="lastName" :counter="10" label="Apellidos" required></v-text-field>
        <v-text-field v-model="email" label="E-mail" required></v-text-field>
      </v-flex>

      <v-flex xs12 sm12 md3 offset-sm1 >
        <v-icon>credit_card</v-icon>
        <v-select v-model="idType" :items="idTypes" label="Tipo de documento" required></v-select>
        <v-text-field v-model="identification" :counter="10" label="Número de documento" required></v-text-field>
        <v-text-field v-model="city" :counter="10" label="Ciudad de residencia" required></v-text-field>

      </v-flex>
      <v-flex xs12 md3 offset-sm1>
        <v-icon>place</v-icon>
        <v-text-field v-model="address" label="Dirección"></v-text-field>
        <v-text-field type="number" v-model="phone" label="Teléfono fijo" ></v-text-field>
        <v-text-field type="number" v-model="cellphone" label="Teléfono celular" ></v-text-field>
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

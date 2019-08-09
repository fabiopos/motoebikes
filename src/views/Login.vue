<template>
  <LoginLayout>
    <v-flex xs12 sm12 md4>
      <v-card class="elevation-12">
        <v-toolbar color="primary" dark flat>
          <v-toolbar-title>Ingresar con redes sociales</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
        <v-card-text>
          <v-container >
            <v-layout wrap align-center>
              <v-flex>
                <v-tooltip bottom>
                  <template v-slot:activator="{ on }">
                    <v-btn large dark color="primary">
                      <span class="pr-5"> ingresar con facebook</span>
                      <v-icon large dark>fab fa-facebook-f</v-icon>
                    </v-btn>
                  </template>
                  <span>Tooltip</span>
                </v-tooltip>
              </v-flex>
               <v-flex >
                <v-tooltip bottom>
                  <template v-slot:activator="{ on }">
                    <v-btn dark class="ml-3"  large color="red">
                      <span class="pr-5"> ingresar con google</span>
                      
                      <v-icon x-large dark>fab fa-google</v-icon>
                    </v-btn>
                  </template>
                  <span>Tooltip</span>
                </v-tooltip>
              </v-flex>
             
               <v-flex >
                <v-tooltip bottom>
                  <template v-slot:activator="{ on }">
                    <v-btn dark class="ml-3"  large color="blue">
                      <span class="pr-5"> ingresar con twitter</span>
                      
                      <v-icon x-large dark>fab fa-twitter</v-icon>
                    </v-btn>
                  </template>
                  <span>Tooltip</span>
                </v-tooltip>
              </v-flex>
            
            </v-layout>
          </v-container>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn to="/" color="primary">Volver</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </LoginLayout>
</template>

<script>
import LoginLayout from "../layouts/LoginLayout";
export default {
  components: {
    LoginLayout
  },
  props: {
    source: String
  },
  data: () => ({
    drawer: null
  })
};
</script>
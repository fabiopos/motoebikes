<template>
    <v-container>

        
        <v-layout text-center wrap>            
            <v-flex offset-sm2 xs12 md12 pa-5>
                <h3 class="headline pa-5">Información del propietario y/o Usuario</h3>
                <RegisterClient />
            </v-flex>
            <v-flex>
            </v-flex>
        </v-layout>

        <v-divider></v-divider>

        <v-layout text-center wrap>            
            <v-flex offset-sm2 xs12 md12 sm12 pa-5>
                <h3 class="headline pa-1">  Descripción del producto</h3>
                <v-icon>motorcycle</v-icon>
                <RegisterVehicle />
            </v-flex>
            <v-flex>
            </v-flex>
        </v-layout>

          <v-layout text-center wrap>            
            <v-flex offset-sm2 xs12 md12 sm12 pa-5>
                <h3 class="headline pa-1">  Estado del vehículo</h3>
                <v-icon>health</v-icon>
                <RegisterVehicleStatus />
            </v-flex>
            <v-flex>
            </v-flex>
        </v-layout>
<v-layout text-right wrap mb-5>
    <v-flex>
         <v-fab-transition>
        <v-btn  class="primary" absolute
                bottom
                dark
                right
                large
                
               > GUARDAR</v-btn>
         </v-fab-transition>
    </v-flex>

</v-layout>
            
    </v-container>

</template>

<script>
import RegisterClient from './client'
import RegisterVehicle from './vehicle'
import RegisterVehicleStatus from './status'
export default {
components:{
    RegisterClient,
    RegisterVehicle,
    RegisterVehicleStatus
}
}
</script>

<style>

</style>

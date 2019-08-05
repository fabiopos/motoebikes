<template>
 
<div>
    <v-layout pa-1 wrap text-left>
      <v-flex xs12 md6>
        <v-card class="pa-5 ma-2" elevation="12"> 
          <v-text-field append-icon="motorcycle" v-model="model" :counter="10" label="Modelo" required></v-text-field>
          <v-text-field append-icon="motorcycle" v-model="color" :counter="10" label="Color" required></v-text-field>
          <v-text-field append-icon="motorcycle" v-model="licensePlate" label="Placa" required></v-text-field>
          <v-text-field append-icon="motorcycle" v-model="chasis" :counter="10" label="Chasis" required></v-text-field>
        </v-card>
        
      </v-flex>

        <v-flex xs12 md5 offset-md1>
          <v-card class="pa-5 ma-2" elevation="12"> 
            <v-subheader>Tipo de servicio</v-subheader>
            <v-radio-group v-model="serviceType">
                  <v-radio
                      v-for="n in serviceTypes"
                      :key="n.id"
                      :label="`${n.name}`"
                      :value="n.name"
                  ></v-radio>
            </v-radio-group>       
            <i class="caption">Recuerde que la inasistencia a las revisiones periódicas 
                puede causar la pérdida de la garantía</i>
          </v-card>
      </v-flex>
      
    </v-layout>
    <!-- <v-layout wrap >
        <h3 class="headline">Accesorios vehículo</h3>
    </v-layout> -->
    <v-divider></v-divider>
    <br>

    <v-card class="pa-5 ma-2" elevation="12"> 
      <v-layout wrap >
          <v-flex xs12 md12>
            <v-subheader>Accesorios recibidos</v-subheader>
          </v-flex>       
      </v-layout>
      <v-layout wrap v-for="(item, index) in vehicleAccesories" :key="index">

          <v-flex xs12 md6>
                        
          <v-switch 
                          v-model="registeredAccesories[item.id].value"
                          class="ma-1"
                          :label="`${item.name}`"        
                        ></v-switch>
        </v-flex>       
        <v-flex xs12 md2>
          <v-text-field type="number" v-if="registeredAccesories[item.id].value" 
          v-model="registeredAccesories[item.id].quantity" 
          :counter="2" label="cantidad" 
          append-icon="camera_alt"
          @click:append="openCamera"
          required></v-text-field>
        </v-flex>
        
      </v-layout>
    </v-card>
    
  </div>
</template>

<script>

export default {
  components:{
     
  },
  data: () => ({
    valid: false,
    model: "",
    color: "",
    licensePlate: "",
    motor: "",
    chasis: "",
    serviceType:"",
    serviceTypes:[
          {
            id:'GAR',
            name: 'Garantía'
        },
        {
            id:'CORT',
            name: 'Cortería comercial'          
        },
        {
            id:'MANT',
            name: 'Mantenimiento'          
        },
        {
            id:'REV_1000',
            name: 'Revisión 1000 kms'
        },
        {
            id:'REV_3000',
            name: 'Revisión 3000 kms'          
        },
          {
            id:'REV_9000',
            name: 'Revisión 9000 kms'
        },
        {
            id:'REV_12000',
            name: 'Revisión 12000 kms'          
        },
          {
            id:'REV_15000',
            name: 'Revisión 15000 kms'
        },
        {
            id:'REV_18000',
            name: 'Revisión 18000 kms'          
        },
          {
            id:'REV_21000',
            name: 'Revisión 21000 kms'
        },
        {
            id:'REV_27000',
            name: 'Revisión 27000 kms'          
        },
          {
            id:'REV_30000',
            name: 'Revisión 30000 kms'
        },
        {
            id:'REV_33000',
            name: 'Revisión 33000 kms'          
        }
      
    ],
    vehicleAccesories:[
        {id: 'AC01', name: 'Baúl con llaves', value: false},
        {id: 'AC02', name: 'LLaves de encendido', value: false},
        {id: 'AC03', name: 'Control de alarma', value: false},
        {id: 'AC04', name: 'Cargador', value: false},
        {id: 'AC05', name: 'Manual de usuario o garantía', value: false},
        {id: 'AC06', name: 'Pedales', value: false},
        {id: 'AC07', name: 'Casco', value: false},
        {id: 'AC08', name: 'Guantes', value: false},
        {id: 'AC09', name: 'Gafas', value: false},
        {id: 'AC10', name: 'Chaleco', value: false},
        {id: 'AC11', name: 'Impermeable', value: false},
        {id: 'AC12', name: 'Tarjeta de propiedad', value: false},
    ],
    registeredAccesories:{
        AC01: {value: false, quantity: 0 },
        AC02:  {value: false, quantity: 0 },
        AC03:  {value: false, quantity: 0 },
        AC04:  {value: false, quantity: 0 },
        AC05:  {value: false, quantity: 0 },
        AC06:  {value: false, quantity: 0 },
        AC07:  {value: false, quantity: 0 },
        AC08:  {value: false, quantity: 0 },
        AC09:  {value: false, quantity: 0 },
        AC10:  {value: false, quantity: 0 },
        AC11:  {value: false, quantity: 0 },
        AC12:  {value: false, quantity: 0 }
    }
    
  }),
  methods:{
      openCamera(){
          alert('Aqui se abre la camara para tomar evidencia del accesorio recibido')
      }
  }
};
</script>

<style>
</style>

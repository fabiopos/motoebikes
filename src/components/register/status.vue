<template>
 
<div>
    <v-layout pa-1 wrap text-left  v-for="n in statusTypes" :key="n.id">
      

        <v-flex xs12 md12 offset-md1 >         
            <v-select :items="['Bueno', 'Regular', 'Malo']" :label="n.name"  v-model="registeredStatus[n.id].status">
            </v-select>
            <v-text-field v-if="registeredStatus[n.id].status !== 'Bueno' && registeredStatus[n.id].status != ''" label="Observaciones" placeholder="escriba un comentario aquí"></v-text-field>
        </v-flex>

      
      
    </v-layout>
    <v-layout pa-1 wrap text-left  v-for="n in batteryStatus" :key="n.id">
    <v-flex xs12 md12 offset-md1 >         
                
                <v-text-field type="number" :label="`${n.name} (Voltaje)`" placeholder="voltaje"></v-text-field>
            </v-flex>
    </v-layout>
    
   
    
  </div>
</template>

<script>
export default {
  data: () => ({
    valid: false,
    model: "",
    color: "",
    licensePlate: "",
    motor: "",
    chasis: "",
    serviceType:"",
    batteryStatus:[
        {
            id: 'BAT01',
            name: 'Batería 1',
            voltage: 0
        },
        {
            id: 'BAT02',
            name: 'Batería 2',
            voltage: 0
        },
        {
            id: 'BAT03',
            name: 'Batería 3',
            voltage: 0
        },
        {
            id: 'BAT04',
            name: 'Batería 4',
            voltage: 0
        },
        {
            id: 'BAT05',
            name: 'Batería 5',
            voltage: 0
        },
        {
            id: 'BAT06',
            name: 'Batería 6',
            voltage: 0
        }
        
    ],
    statusTypes:[
        {
            id:'ST01',
            name: 'Pintura en General'
        },
        {
            id:'ST02',
            name: 'Suspensión delantera'          
        },
          {
            id:'ST03',
            name: 'Sistema de frenos'
        },
        {
            id:'ST04',
            name: 'Guayas freno trasero'          
        },
          {
            id:'ST05',
            name: 'Rin y llanta delantera'
        },
        {
            id:'ST06',
            name: 'Presión de inflado'          
        },
          {
            id:'ST07',
            name: 'Soporte lateral'
        },
        {
            id:'ST08',
            name: 'Soporte central'          
        },
          {
            id:'ST09',
            name: 'Posapies Del / Tras'
        },
        {
            id:'ST10',
            name: 'Suspensión trasera'          
        },
          {
            id:'ST11',
            name: 'Rueda trasera'
        },
        {
            id:'ST12',
            name: 'Motor'          
        },
        {
            id:'ST13',
            name: 'Porta placa'          
        },
        {
            id:'ST14',
            name: 'Cajuela sillín'          
        },
        {
            id:'ST15',
            name: 'Tapicería sillín'          
        },
        {
            id:'ST16',
            name: 'Cubiertas traseras'          
        }
    ],
  
    registeredStatus:{
        ST01: { value: false, quantity: 0, status: '' },
        ST02:  {value: false, quantity: 0, status: '' },
        ST03:  {value: false, quantity: 0, status: '' },
        ST04:  {value: false, quantity: 0, status: '' },
        ST05:  {value: false, quantity: 0, status: '' },
        ST06:  {value: false, quantity: 0, status: '' },
        ST07:  {value: false, quantity: 0, status: '' },
        ST08:  {value: false, quantity: 0, status: '' },
        ST09:  {value: false, quantity: 0, status: '' },
        ST10:  {value: false, quantity: 0, status: '' },
        ST11:  {value: false, quantity: 0, status: '' },
        ST12:  {value: false, quantity: 0, status: '' },
        ST13:  {value: false, quantity: 0, status: '' },
        ST14:  {value: false, quantity: 0, status: '' },
        ST15:  {value: false, quantity: 0, status: '' },
        ST16:  {value: false, quantity: 0, status: '' }
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

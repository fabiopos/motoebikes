<template>
    <div>
         <section>
        <v-parallax :src="require('./assets/motor_home_1.jpg')" >
          <v-layout column align-center justify-center class="white--text">
            <h1 class="white--text mb-2 display-1 text-xs-center" style="font-weight: 900; text-shadow: 3px 2px #000000">La mejor opción para su moto</h1>
            <div class="white--text subheading mb-3 text-xs-center" style="font-weight: 900; text-shadow: 2px 2px #000000">sin salir de casa</div>
            <v-btn class="cyan lighten-2 mt-5" dark large href="/pre-made-themes">
              Empezar ahora
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-layout
          column
          wrap
          class="my-5"
          align-center
        >
          <v-flex xs12 sm4 class="my-3">
            <div class="text-xs-center">
              <h2 class="headline">La mejor opción en el sector de las dos ruedas </h2>
              <span class="subheading">
                No más demoras, no más límites
              </span>
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card class="elevation-3 transparent">
                    <v-card-text class="text-xs-center text-center">
                      <v-icon x-large class="blue--text text--lighten-2">public</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Todo desde el celular</div>
                    </v-card-title>
                    <v-card-text>
                      Cualquier servicio que contrate puede monitorearlo en tiempo real y si desea adicionar mejoras a
                      su vehículo, podrá hacerlo sin necesidad de desplazarse hasta el taller.
                      ¿Quiere cotizar un repuesto? en nuestra aplicación podrá hacerlo y consultar en que lugar lo puede adquirir.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-8 transparent">
                    <v-card-text class="text-xs-center text-center">
                      <v-icon x-large class="blue--text text--lighten-2">flash_on</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline">Contrate un servicio</div>
                    </v-card-title>
                    <v-card-text>
                        Si desea una revisión para su moto, nosotros somos la mejor opción. 
                      Contamos con al menos <strong>10.000</strong> talleres asociados en la ciudad de Bogotá
                      que te pueden ayudar con lo que necesites para tu vehículo.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card class="elevation-3 transparent">
                    <v-card-text class="text-xs-center text-center">
                      <v-icon x-large class="blue--text text--lighten-2">location_on</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-xs-center">Sitios cercanos</div>
                    </v-card-title>
                    <v-card-text>
                      Encuentre el taller más cercano a través de nuestra aplicación y
                      consulte la ubicación de los talleres habilitados en  la ciudad de Bogotá
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
        <v-parallax :src="require('./assets/background3.jpg')" height="380">
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-3 text-xs-center">
              Empieza ahora y recibe un cupón de descuento en tu primera servicio de mantenimiento </div>
            <em>Todos los vehículos electricos tienen un descuento adicional en algunos talleres en la ciudad de Bogotá</em>
            <v-btn class="blue lighten-2 mt-5" dark large href="/pre-made-themes">
              Empezar ahora
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

       <section>
        <v-container grid-list-md>

        
          <v-layout row wrap>
          <v-flex xs12 text-center class="mt-5">
           <div class="headline">Ya te impresionamos lo suficiente?</div>
           <br>
          <div>Déjanos enviarte un brochure por email!</div>
          </v-flex>
          <v-flex xs8 offset-xs2>

              <v-card class="elevation-5 transparent">

                <v-card-text>
                  <v-flex xs12 v-if="!subscribed">
                    <v-text-field box label="Correo electrónico" :rules="emailRules" v-model="email" hint="Ingresa tu email!" persistent-hint></v-text-field>
                  </v-flex>
                  <v-flex xs12 v-if="!subscribed">
                    <v-text-field box multi-line label="Intereses y curiosidades" hint="Escribe aquí que cosas te pueden interesar del mundo de las dos ruedas" persistent-hint></v-text-field>
                  </v-flex>
                  <v-flex xs12 class="text-xs-center" v-if="!subscribed">
                    <v-btn class="blue lighten-2 mb-5" dark large @click="subscribe">Enviar brochure</v-btn>
                  </v-flex>
                   <v-flex xs12 class="text-xs-center" v-if="subscribed">
                    <v-btn class="green lighten-2 mb-5" dark large>Welcome on board!</v-btn>
                  </v-flex>
                </v-card-text>

             </v-card>

                </v-flex>
            </v-layout>
          </v-container>
      </section>

       <section>
       <v-parallax :src="require('./assets/background3.jpg')" height="380">
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-3 text-xs-center">
              Nuestras redes sociales</div>
              <em>para estar al día con nuestras promociones y eventos</em>
          </v-layout>
          <v-layout justify-space-around justify-center>

              <v-icon x-large dark>fab fa-facebook-f</v-icon>

              <v-icon x-large dark>fab fa-twitter</v-icon>             

              <v-icon x-large dark>fab fa-instagram</v-icon>

             
            </v-layout>
        </v-parallax>
      </section>

      <section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-5">
            <v-flex xs12 sm4>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Acerca de nosotros</div>
                </v-card-title>
                <v-card-text>
                  No somos una compañía, más bien somos un acompañamiento para que las personas puedan acceder a los 
                  servicios de un taller sin complicaciones, sin esperas, con un respaldo, con buenos precios.
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card class="elevation-0 transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Y que tal un upgrade a mi moto?</div>
                </v-card-title>
                <v-card-text>
                  Te ofrecemos todo lo necesario para que tu moto esté al día con el mantenimiento y adicionalmente
                  te podemos recomendar los upgrades (personalizaciones, accesorios, lujos) o un plan como los puedes ejecutar.
                </v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>

       <section>
        
     </section>

    


      <v-footer class="blue darken-2">
        <v-layout row wrap align-center>
          <v-flex>
             <img height="50px" :src="require('./assets/logo.png')">
          </v-flex>
          <v-flex xs11 class="text-right">
            <div class="white--text ml-3">
              Bogotá, Colombia
              <br>         
              Powered by
              <span class="yellow--text">@motoEBikes</span>
            </div>
          </v-flex>
        </v-layout>
      </v-footer>
    </div>
</template>

<script>
export default {

}
</script>

<style>

</style>

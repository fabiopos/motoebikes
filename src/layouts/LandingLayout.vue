<template>
 <div>
    <v-toolbar class="white">
     <v-toolbar-side-icon>
       <img :src="require('../assets/logo.png')" alt="Vuetify.js" height="60px"></v-toolbar-side-icon>
      <v-toolbar-title class="mx-0" v-text="title"></v-toolbar-title>
     
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn to="login" class="primary" dark flat>Ingresar</v-btn>
        <!--<v-btn flat>Blog</v-btn>-->


        <!-- <v-btn icon to="/register" dark class="primary">
        
            <v-icon>person</v-icon>
        </v-btn> -->
      </v-toolbar-items>
    </v-toolbar>
    <v-content>
        <slot />
    </v-content>    

 </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },
  created(){
    console.log(this.$router.currentRoute.path)
  },
  data: () => ({
      title: "motoEBikes",
      subscribe: false,
      imageLink: {
        main:
          "https://firebasestorage.googleapis.com/v0/b/endorfinevue.appspot.com/o/assets%2Fb13f0434-b228-11e6-8e5d-5252025056ab_web_scale_0.4666667_0.4666667__.jpg?alt=media&token=660df23e-599e-434b-9313-ba69c973eeea",
        sub_main:
          "https://firebasestorage.googleapis.com/v0/b/endorfinevue.appspot.com/o/assets%2FNight-Club-Clubbing-Jobs-Abroad2.jpg?alt=media&token=82bbda7d-5df4-430b-9217-adaf1c8485c5",
        logo:
          "assets/logo.png",
        social_cover:
          "https://firebasestorage.googleapis.com/v0/b/endorfinevue.appspot.com/o/assets%2Fo-NIGHTCLUB-facebook.jpg?alt=media&token=cefc5c4c-9714-41da-9c22-f63caf5e89a4"
      },
      email: "",
      emailRules: [
        v => {
          return !!v || "E-mail is required";
        },
        v =>
          /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) ||
          "E-mail must be valid"
      ],
      subscribed: false
    }
  ),
};
</script>
<style>
a{
  text-decoration: none;
  color:inherit;
}
</style>


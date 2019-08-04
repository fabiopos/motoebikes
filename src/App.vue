<template>
  <v-app>
    <v-app-bar app>

      <!-- toolbar begins -->
      <v-toolbar-title class="headline text-uppercase">
        <a href="/">
          <span>motoEBikes</span>
        <span class="font-weight-light"> platform</span>
        </a>
        
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="#"
        target="_blank"
      >
        <span class="mr-2">v1.0</span>
      </v-btn>
    </v-app-bar>
    <!-- toolbar ends -->
    
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
    
  },
  data: () => ({
    //
  }),
};
</script>
<style>
a{
  text-decoration: none;
  color:inherit;
}
</style>


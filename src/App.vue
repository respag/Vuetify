<template>
  <v-app class="container">
    <v-app-bar app color="deep-purple accent-4">
      <v-toolbar-title class="headline text-uppercase yellow--text">
        <span>Respag</span>
        <span class="font-weight-light"> SCHOOL</span>
      </v-toolbar-title>
       <div class="flex-grow-1"></div>
       <v-toolbar-items>
         <v-btn text router-link to="/" class="white--text">Inicio</v-btn>   
         <v-btn text router-link to="/alertas" class="white--text">Alertas</v-btn> 
       </v-toolbar-items>
      <v-spacer></v-spacer>
      <v-btn text href="https://github.com/vuetifyjs/vuetify/releases/latest" target="_blank" class="white--text">
        <span class="mr-2">Latest Release</span>
        <v-icon>fas fa-external-link-alt</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>

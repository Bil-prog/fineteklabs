<template>
  <v-app>
    <v-app-bar
      app
      color="white"
      
    >
        
      <v-toolbar-title
        black--text
        font-weight-bold
      ><strong>Fineteklabs</strong></v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  data: () => ({
    //
  
  }),
};
</script>

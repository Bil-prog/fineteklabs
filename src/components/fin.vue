<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
          
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

     <div class="d-flex flex-row mb-6">
      <v-card-text class="white--text pt-0">
       Finetek is a software development company based in Nairobi Kenya, established in 2016, Finetek has had a remarkable experience in development of innovative software solutions to cater for various client needs
      </v-card-text>

       <v-card-text class="white--text pt-0">
       Finetek is a software development company based in Nairobi Kenya, established in 2016, Finetek has had a remarkable experience in development of innovative software solutions to cater for various client needs
      </v-card-text>
     </div>  

      <v-divider></v-divider>

  
      <v-card-text class="blue white--text">
        {{ new Date().getFullYear() }} — <strong>Finetek Technologies K Ltd <v-spacer></v-spacer> info@fineteklabs.com  <v-spacer></v-spacer> +254 734 34 1962</strong>
      </v-card-text>  
    </v-card>
  </v-footer>
</template>

<script>
export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-linkedin',
      ],
    }),

}
</script>

<style>

</style>
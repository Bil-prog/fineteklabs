<template>
   <v-card
    max-width="1500"
    class="mx-auto"
    outlined
  >
    <v-container 
    class="pa-1"
    max-width="900"
    >
      <v-item-group
        multiple
      >
        <v-row class="d-flex justify-center mb-6">
          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12"
            sm="4"
          >
            <v-item>
              <v-img
                :src="item.src"
              >

              </v-img>
            </v-item>
          </v-col>
        </v-row>
      </v-item-group>
    </v-container>
  </v-card>
</template>

<script>
export default {
     data: () => ({
      items: [
        {
          src: 'buruk.png',
        },
        {
          src: 'falconsigns.jpg',
        },
        {
          src: 'hhour.png',
        },
        {
          src: 'papcon.jpg',
        },
        {
          src: 'perfectpics.png',
        },
        {
          src: 'sucafina.svg',
        },
        {
          src: 'ktb.png',
        },
        {
          src: 'newnham.png',
        },
        {
          src: 'mnc.png',
        },
        {
          src: 'povo.png',
        },
        {
          src: 'canopy.png',
        },
        {
          src: 'ideas.png',
        },

      ],
    }),

}
</script>

<style>

</style>
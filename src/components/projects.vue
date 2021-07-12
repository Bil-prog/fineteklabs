<template>
  <v-card
    max-width="1400"
    class="mx-auto"
  >
    <v-container class="pa-1">
      <v-item-group
        multiple
      >
        <v-row>
          <v-col
            v-for="(item, i) in items"
            :key="i"
            cols="12"
            sm="4"
          >
            <v-item>
              <v-img
                :src="item.src"
                height="330"
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
          src: 'img_01.PNG',
        },
        {
          src: 'img_02.PNG',
        },
        {
          src: 'img_03.PNG',
        },
      ],
    }),
  }
</script>

<style>

</style>
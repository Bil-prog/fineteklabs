<template>
<div class="home">
  <v-carousel
    cycle
    height="580"
    hide-delimiter-background
    show-arrows-on-hover
    dark
    class="hidden-sm-and-down"
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        :color="colors[i]"
        height="100%"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="text-h2 white--text">
            {{ slide }} 
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>

    <v-carousel
    cycle
    height="580"
    hide-delimiter-background
    show-arrows-on-hover
    dark
    class="hidden-md-and-up"
    v-model="model"
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        :color="colors[i]"
        height="100%"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
          style="padding-left: 40px;"

        >
          <div class="text-h2 white--text">
            {{ slide }} 
          </div>
        </v-row>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>

  <h2 class="text-center teal--text">Our Services</h2>

  <timeline />

  <h1 class="text-center blue--text">Why us?</h1>
  <h3 class="text-center font-weight-thin">Why work with finetek Technologies K Ltd?</h3>

<br>

<expansion />

<br>

  <h1 class="text-center red--text">Projects</h1>
  <h3 class="text-center font-weight-thin">Our digital solutions</h3>

<Projects />

<br>
 
 <h1 class="text-center blue--text">Clients</h1>
 <h3 class="text-center font-weight-thin">Our client profile</h3>

<br>
<Clients />
<br>

<Fin />
</div>
</template>



<script>
import timeline from '../components/timeline.vue';
import expansion from '../components/expansion.vue'
import Projects from '../components/projects.vue';
import Clients from '../components/clients.vue';
import Fin from '../components/fin.vue';
 export default {
  components: { timeline, expansion, Projects, Fin, Clients },
  
    data () {
      return {
        model: 0,
        colors: [
          '#F44336',
          'warning',
          '#1A237E',
          '#03A9F4',
          '#000000',
        ],
        slides: [
          'Innovative Digital Solutions',
          'E-commerce Solutions',
          'Customised Software Solutions',
          'Financial Service Solutions',
          'Go beyond, Grow beyond',
        ],
      }
    },
  }
</script>


<style>



</style>

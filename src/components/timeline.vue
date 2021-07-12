<template>
<v-container max-width="1000">
  <v-timeline
    align-top
    :dense="$vuetify.breakpoint.smAndDown"
  >
    <v-timeline-item
      v-for="(item, i) in items"
      :key="i"
      :color="item.color"
      :icon="item.icon"
      :title="item.title"
      :content="item.content"
      fill-dot
    >
      <v-card
        :color="item.color"
        dark
      >
        <v-card-title  class="text-h6">
         <v-icon :style="{right: '2%'}">{{ item.icon }}</v-icon> {{ item.title }}
        </v-card-title>
        <v-card-text class=" text--white">
          <p>{{ item.content }}</p>
             <div class="my-2">
           <Popup />
          </div>
        </v-card-text>
      </v-card>
    </v-timeline-item>
    
  </v-timeline>
  </v-container>
</template>

<script>
import Popup from '../components/popup.vue';
export default {
  components: { Popup },
    data: () => ({
      items: [
        { 
          title: 'Payments',  
          content: 'We offer financial services integration and management for e-commerce and other businesses',  
          color: '#2196F3',
          icon: 'mdi-bank',
        },
        {
          title: 'Business',  
          content: 'We offer varied business management solutions for businesses such as ERP systems,POS systems,Payroll systems to help improve efficiency, business management and operations in general',  
          color: '#000000',
          icon: 'mdi-rocket',
        },
        {
          title: 'Commerce',  
          content: 'We help you put your business up and running through development of e-commerce solutions on the go , depending on your industry',  
          color: '#FFB300',
          icon: 'mdi-cart',
        },
        {
          title: 'Agritech',  
          content:'Through our innovative approach, we help customise agritech solutions to meet the industry needs for growth',  
          color: '#43A047',
          icon: 'mdi-cogs',
        },
        {
          title: 'Finance',  
          content: 'We customise financial solutions to enable traditional businesses and informal sector persons access banking solutions',  
          color: '#EF5350',
          icon: 'mdi-store',
        },
        {
          title: 'Custom',  
          content: 'We develop custom software solutions, android apps , IoT solutions to cater our customer needs',  
          color: '#283593',
          icon: 'mdi-monitor-cellphone',
        },
      ],
    }),

}
</script>

<style>

</style>
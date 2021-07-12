<template>
  <v-row justify="center">
    <v-expansion-panels popout>
      <v-expansion-panel
        v-for="(item,i) in items"
        :key="i"
         :title="item.title"
         :content="item.content"
      >
        <v-expansion-panel-header class="font-weight-bold">{{ item.title }}</v-expansion-panel-header>
        <v-expansion-panel-content>
          {{ item.content }}
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-row>
</template>

<script>
export default {
    data: () => ({
      items: [
        { 
          title: 'Innovative process',  
          content: 'We offer an innovative approach to doing our system design and implementation'
        },
        {
           title: 'High experience',  
           content: 'Our team comprises of highly experienced professionals with know how of modern tech landscape'
          
        },
        {
          title: 'Decisiveness',  
          content: 'You give us your problem, we offer you a lasting solution'
        },
        {
         title: 'Going beyond',  
          content: 'we ensure as we go beyond our boundaries of innovation, research and development, we grow beyond our limits'
        },
       
      ],
    }),

}


</script>

<style>

</style>
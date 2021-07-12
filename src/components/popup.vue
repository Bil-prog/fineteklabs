<template>
  
  <v-row justify="right">
    <v-dialog
      v-model="dialog"
      persistent
      max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
         <v-btn
              color="#EF5350"
              fab
              small
              dark
              v-bind="attrs"
              v-on="on"
            >
              <v-icon>mdi-plus</v-icon>
            </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">Request Quote</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
            <v-col
                cols="12"
              >
                <v-autocomplete
                  :items="['E-commerce solution', 'Financial services', 'Mobile application', 'Application',]"
                  label="Select Service"
                  multiple
                  prepend-icon="mdi-chart-bubble"
                ></v-autocomplete>
              </v-col>

             <v-col
                cols="12"
             >
             <v-text-field
             label="Company Name*"
             required
             prepend-icon="mdi-folder"
             :rules="inputRules"
             >
             </v-text-field>
             </v-col>
              
              <v-col
                cols="12"
              >
                <v-textarea
                  label="Request*"
                  required
                  prepend-icon="mdi-pencil"
                ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Telephone"
                  required
                  prepend-icon="mdi-pencil"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                  label="Email*"
                  required
                  prepend-icon="mdi-email"
                ></v-text-field>
              </v-col>             
            </v-row>
          </v-container>
          <small>*indicates required field</small>
          <v-spacer></v-spacer>
          <small class="red--text">Hot-line:+254 734 34 19 62</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="blue darken-1"
            @click="dialog = false"
          >
            Cancel
          </v-btn>
          <v-btn
            color="blue darken-1"
            @click="dialog = false"
          >
            request quote
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>


<script>
export default {
    data: () => ({
      dialog: false,
    }),

    pass() {
        return {
            inputRules: [
                v => v.length >=3 || 'Minimum length is 3 characters',
            ],
        }


    }
    

}
</script>

<style>

</style>
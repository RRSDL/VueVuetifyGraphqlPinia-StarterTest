<template> 
  <v-card class="text-center fill-height ma-2 bg-brown-lighten-3 text-grey-darken-4" >
    <v-card-title class="font-weight-black">
        Rocket Name: {{ rocket_details.name }}
    </v-card-title>
        
    <v-card-subtitle class="font-weight-bold">
      First Flight: {{ rocket_details.first_flight }} <br>
      Height: {{ rocket_details.height.feet }} <br>
      Diameter: {{ rocket_details.diameter.meters }}
          
    </v-card-subtitle>
        
    <v-card-text>
        
        Description: {{ rocket_details.description }}
    </v-card-text>
  </v-card>
</template>

<script setup>
  const { rocket_details } = defineProps(['rocket_details'])
</script>

<style scoped>

</style>
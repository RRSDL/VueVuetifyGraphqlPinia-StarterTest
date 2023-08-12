<template> 
  <v-card class="text-center fill-height ma-2 bg-brown-lighten-3 text-grey-darken-4" >
    <v-card-title class="font-weight-black">
        Mission Name:
        {{ rocket_launches.mission_name }}
    </v-card-title>
        
    <v-card-subtitle class="font-weight-bold">
        Rocket Name: {{ rocket_launches.rocket.rocket_name }}
          
    </v-card-subtitle>
        
    <v-card-text>
        Launch Date: {{ rocket_launches.launch_date_local }} <br>
        Launch Site Name: {{ rocket_launches.launch_site }} <br>
        <strong>Details: </strong> <br>
        {{ rocket_launches.details }}
    </v-card-text>
  </v-card>
</template>

<script setup>
  const { rocket_launches } = defineProps(['rocket_launches'])
</script>

<style scoped>

</style>
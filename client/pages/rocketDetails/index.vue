<template>
  <div>
    <v-container class="fluid py-16">
      <v-row class="mx-auto">
        <v-col 
          v-for="rckt in data.rockets"
          :key="rckt.name"
          cols="12" sm="10" md="8" lg="6"
        >
          <rocketDetailsCard :rocket_details="rckt"/>
        </v-col>
      </v-row>
    </v-container>
    </div>
</template>

<script setup>
  definePageMeta ({
    layout: 'rocketlaunchesandrocketdetails'
  }) 

  const query = gql`
  query getRockets{
  rockets {
    name
    first_flight
    height {
      feet
    }
    description
    diameter {
      meters
    }
    mass {
      kg
    }
    stages
  }
}
`

const { data } = useAsyncQuery(query)

</script>

<style lang="scss" scoped>

</style>
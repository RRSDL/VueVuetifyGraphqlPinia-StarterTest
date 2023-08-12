<template>
  <div>
    <div class="text-center py-15">
      <input 
      type="text"
      placeholder="Search Year"
      class="searchbar"
      v-model="searchValue"
      >
      {{ searchValue }}
    </div>
    <div class="bg-red">{{ searchValue }}</div>
    <v-container class="fluid py-16">
      <v-row class="mx-auto">
        <v-col 
          v-for="rckt in data.launches"
          :key="rckt.rocket.rocket_name"
          cols="12" sm="10" md="8" lg="6"
        >
          <rocketLaunchesCard :rocket_launches="rckt"/>
        </v-col>
      </v-row>
    </v-container>
    
  </div>
</template>

<script setup>

{
  data: () => ({
    searchValue: '',
  })
}

  definePageMeta ({
    layout: 'rocketlaunchesandrocketdetails'
  }) 

  const query = gql`
	query getLaunches {
  launches {
    mission_name
    launch_date_local
    launch_site {
      site_name
    }
    rocket {
      rocket_name
    }
    details
  }
}
`
const { data } = useAsyncQuery(query)

</script>

<style scoped>

::placeholder {
  color: black;
  opacity: 1;
}
  .searchbar {
    padding: 10px;
    background-color: grey;
    border-radius: 4px;
  }

</style>
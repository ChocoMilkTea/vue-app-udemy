<template>
  <v-app>
    <v-container fluid>
      <v-tabs>
        <v-tab>Getting Started</v-tab>
          <v-tab-item>
            <GettingStarted/>
          </v-tab-item>
        <v-tab>Assignment 1</v-tab>
          <v-tab-item>
            <Assignment1/>
          </v-tab-item>
        <v-tab>Assignment 2</v-tab>
          <v-tab-item>
            Nothing Yet
          </v-tab-item>
      </v-tabs>    
      
      <router-view/>
    </v-container>
  </v-app>
</template>

<script>
  import GettingStarted from '@/components/GettingStarted'
  import Assignment1 from '@/components/Assignment1'

  export default {
    name: 'App',
    components: {
      GettingStarted,
      Assignment1
    }    
  }
  
</script>
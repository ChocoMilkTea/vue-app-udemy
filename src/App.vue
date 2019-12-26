<template>
  <v-app>      
    <v-container fluid>
      <v-tabs>
        <v-tab>Udemy</v-tab>
          <v-tab-item>
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
                  <Assignment2/>
                </v-tab-item>
              <v-tab>Assignment 3</v-tab>
                <v-tab-item>
                  <Assignment3/>
                </v-tab-item>
              <v-tab>Assignment 4</v-tab>
                <v-tab-item>
                  <Assignment4/>
                </v-tab-item>
            </v-tabs>    
          </v-tab-item>
        <v-tab>Monster Slayer</v-tab>
          <v-tab-item>
            
          </v-tab-item>
        <v-tab>Testing Playground</v-tab>
          <v-tab-item>
            <Playground/>
          </v-tab-item>
      </v-tabs>      
      
      <router-view/>
    </v-container>
  </v-app>
</template>

<script>
  import GettingStarted from '@/components/GettingStarted'
  import Assignment1 from '@/components/Assignment1'
  import Assignment2 from '@/components/Assignment2'
  import Assignment3 from '@/components/Assignment3'
  import Assignment4 from '@/components/Assignment4'
  import Playground from '@/components/Playground'
  
  export default {
    name: 'App',
    components: {
      Playground,
      GettingStarted,
      Assignment1,
      Assignment2,
      Assignment3,
      Assignment4
    }    
  }
  
</script>
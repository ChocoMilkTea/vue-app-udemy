<template>
  <div>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 1</v-card-title>
          <v-card-subtitle>Dynamic styling</v-card-subtitle>          
          <v-card-actions>
            <div 
              class="demo" 
              @click="attachRed = !attachRed" 
              :class="divClasses"></div>
            <div class="demo" :class="{red: attachRed}"></div>
            <div class="demo" :class="[color, {red: attachRed}]"></div>
            <v-spacer></v-spacer>
            <v-text-field v-model="color"></v-text-field>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>    
  </div>
</template>

<style>
  .demo {
    width: 100px;
    height: 100px;
    background-color: gray;
    display: inline-block;
    margin: 10px;
  }
  
  .red {
    background-color: red;
  }

  .green {
    background-color: green;
  }

  .blue {
    background-color: blue;
  }
</style>

<script>
  export default {
    name: 'Assignment3',
    data: () => ({
      attachRed: false,
      color: 'green'
    }),
    computed: {
      divClasses() {
        return {
          red: this.attachRed,
          blue: !this.attachRed
        }
      }
    }
  }
</script>

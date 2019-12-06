<template>
  <div>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 1</v-card-title>
          <v-card-subtitle>Counter to increase on click</v-card-subtitle>
          <v-card-text>
            <v-btn v-on:click="increase(2, $event)">Click Me</v-btn>
            <p>Counter: {{ counter }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 2</v-card-title>
          <v-card-subtitle>Update coordinates of move cursor</v-card-subtitle>
          <v-card-text>
            <p v-on:mousemove="updateCoordinates">
              Coordinates: {{ x }} / {{ y }}
              - <span v-on:mousemove="dummy">DEAD SPOT</span>      
            </p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>    
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 3</v-card-title>
          <v-card-subtitle>Listening to key event</v-card-subtitle>          
          <v-text-field v-on:keyup.native="alertMe"></v-text-field>
        </v-card>
      </v-col>
    </v-row>
  </div>  
</template>

<style>
</style>

<script>
  export default {
    name: 'Assignment1',
    data: () => ({
      counter: 0,
      x: 0,
      y: 0
    }),
    methods: {
      increase(step, event) {
        this.counter += step;
        event; // Just to supress warning
      },
      updateCoordinates(event) {
        this.x = event.clientX;
        this.y = event.clientY;
      },
      dummy(event) {
        event.stopPropagation();
      },
      alertMe() {
        alert('Alert!');
      }
    }

  }
</script>

<template>
  <div>
    <v-btn>Click Me</v-btn>
    <p>{{ counter }}</p>
    <p v-on:mousemove="updateCoordinates">
      Coordinates: {{ x }} / {{ y }}
      - <span v-on:mousemove="dummy">DEAD SPOT</span>      
    </p>
    
    {{y}}
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
      increase(step) {
        this.counter += step;
      },
      updateCoordinates(event) {
        this.x = event.clientX;
        this.y = event.clientY;
      },
      dummy(event) {
        event.stopPropagation();
      }
    }

  }
</script>

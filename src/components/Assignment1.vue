<template>
  <div>
    <button v-on:click="increase(2, $event)">Click Me</button>
    <p>{{ counter }}</p>
    <p v-on:mousemove="updateCoordinates">
      Coordinates: {{ x }} / {{ y }}
      - <span v-on:mousemove="dummy">DEAD SPOT</span>
      <!-- - <span v-on:mousemove.stop="">DEAD SPOT</span> -->
      <!-- - <span v-on:mousemove.stop.prevent="">DEAD SPOT</span> -->
    </p>
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
        event; // Not in use. Just to stop the error from appearing.
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

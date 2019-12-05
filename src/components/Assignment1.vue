<template>
  <div>
    <button v-on:click="increase">Click Me</button>
    <p>{{ counter }}</p>
    <p v-on:mousemove="updateCoordinates">Coordinates: {{ x }} / {{ y }}</p>
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
      increase() {
        this.counter++;
      },
      updateCoordinates(event) {
        this.x = event.clientX;
        this.y = event.clientY;
      }
    }

  }
</script>

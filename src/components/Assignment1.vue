<template>
  <div>
    <button v-on:click="increase">Click Me</button>
    <p>{{ counter }}</p>
  </div>
</template>

<style>
</style>

<script>
  export default {
    name: 'Assignment1',
    data: () => ({
      counter: 0
    }),
    methods: {
      increase() {
        this.counter++;
      }
    }

  }
</script>

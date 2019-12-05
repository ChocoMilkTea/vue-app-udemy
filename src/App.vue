<template>
  <div id="app">
    <p>{{ sayHello() }}</p>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data: () => ({
      title: 'Hello World!'
    }),
    methods: {
      sayHello() {
        return 'Hello!';
      }
    }
  }
  
</script>
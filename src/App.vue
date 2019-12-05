<template>
  <div id="app">
    <p>
      {{ sayHello() }} - <a v-bind:href="link">Google</a>
    </p>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data: () => ({
      title: 'Hello World!',
      link: 'http://www.google.com'
    }),
    methods: {
      sayHello() {
        return this.title;
      }
    }
  }
  
</script>
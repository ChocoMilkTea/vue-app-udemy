<template>
  <div id="app">
    <h1 v-once>{{ title }}</h1>
    <p>      
      {{ sayHello() }} - <a v-bind:href="link">Google</a>
    </p>
    <hr>
    <p v-html="finishedLink"></p>
  </div>
</template>

<script>
  export default {
    name: 'app',
    data: () => ({
      title: 'Hello World!',
      link: 'http://www.google.com',
      finishedLink: '<a href="http://google.com">Google</a>'
    }),
    methods: {
      sayHello() {
        this.title = 'Hello!';
        return this.title;
      }
    }
  }
  
</script>
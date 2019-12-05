<template>
  <div id="app">
    <GettingStarted/>    
    <hr>
    <Assignment1/>
  </div>
</template>

<script>
  import GettingStarted from '@/components/GettingStarted.vue';
  import Assignment1 from '@/components/Assignment1.vue';

  export default {
    name: 'app',
    components: {
      GettingStarted,
      Assignment1
    }
  }
</script>
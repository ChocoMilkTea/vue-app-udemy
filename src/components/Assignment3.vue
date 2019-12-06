<template>
  <div>
    <div 
      class="demo" 
      @click="attachRed = !attachRed" 
      :class="{red: attachRed}"></div>
    <div class="demo"></div>
    <div class="demo"></div>
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
      attachRed: false
    })
  }
</script>

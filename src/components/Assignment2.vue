<template>
  <div>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 1</v-card-title>
          <v-card-subtitle>Dynamic binding of data</v-card-subtitle>
          <v-card-text>
            <v-text-field v-model="name"></v-text-field>
            <p>{{ name }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 2</v-card-title>
          <v-card-subtitle>Reacting to changes with computed/watch properties</v-card-subtitle>
          <v-card-text>
            <p>Counter: {{ counter }}</p>
            <p>Second Counter: {{ secondCounter }}</p>
            <p>Result: {{ displayResult() }} | {{ output }}</p>
          </v-card-text>
          <v-card-actions>
            <v-btn v-on:click="counter++">Increase</v-btn>
            <v-btn v-on:click="counter--">Decrease</v-btn>
            <v-btn v-on:click="secondCounter++">Increase Second</v-btn>
            <v-btn v-on:click="reset">Reset</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 3</v-card-title>
          <v-card-subtitle>Saving Time with shorthands</v-card-subtitle>          
          <v-card-actions>
            <v-btn @click="changeLink">Click to change link</v-btn>
            <a :href="link">Link</a>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </div>  
</template>

<script>
  export default {
    name: 'Assignment2',
    data: () => ({
      name: 'Thanos',
      counter: 0,
      secondCounter: 0,
      result: '',
      link: 'http://google.com'
    }),
    computed: {
      // for caching result
      // best practise
      // more optimised
      output() {
        console.log('computed');
        return this.counter > 5 ? 'Greater than 5' : 'Smaller than 5';
      }
    },
    watch: {
      // good for aync
      counter(value) {
        var vm = this;
        if (value > 10) {
          setTimeout(function() {
            vm.counter = 0;
          }, 2000);
        }
      }
    },
    methods: {
      // for calling every changes
      displayResult() {
        console.log('method');
        return this.counter > 5 ? 'Greater than 5' : 'Smaller than 5';
      },
      reset() {
        this.counter = 0;
        this.secondCounter = 0;
        this.result = '';
      },
      changeLink() {
        this.link = 'http://apple.com'
      }
    }
  }
</script>


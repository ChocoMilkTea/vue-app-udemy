<template>
  <div>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 1</v-card-title>
          <v-card-subtitle>Print out text</v-card-subtitle>
          <v-card-text>
            <h1 v-once>{{ title }}</h1>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 2</v-card-title>
          <v-card-subtitle>Print out using function and binding of a link</v-card-subtitle>
          <v-card-text>
            <p>
              {{ sayHello() }} - <a v-bind:href="link">Google</a>
            </p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 3</v-card-title>
          <v-card-subtitle>Print out raw html</v-card-subtitle>
          <v-card-text>
            <p v-html="finishedLink"></p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>        
    
  </div>  
</template>

<script>
  export default {
    name: 'GettingStarted',
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
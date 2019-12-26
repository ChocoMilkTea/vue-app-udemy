<template>
  <div>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 1</v-card-title>
          <v-card-subtitle>Conditional Rendering with if-else</v-card-subtitle>
          <v-card-text>
            <p v-if="show">You can see me!<span>Hello!</span></p>
            <p v-else-if="abc">Now you see me!</p>
            <p v-else>Only now you see me!</p>          
            <p v-show="show">Do you also see me?</p>
            <template v-if="show">
              <h1>Heading</h1>
              <p>Inside a template</p>
            </template>
          </v-card-text>
          <v-card-actions>
            <v-btn @click="show = !show">Switch</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-card dark>
          <v-card-title>Task 2</v-card-title>
          <v-card-subtitle>Rendering list with v-for</v-card-subtitle>
          <v-card-text>
            <ul>
              <li v-for="(ingredient, i) in ingredients" v-bind:key ="ingredient">{{ ingredient }} ({{ i }})</li>
            </ul>
            <v-btn @click="ingredients.push('spices')">Add New</v-btn>
            <hr>
              <li v-for="person in persons" v-bind:key="person">
                <div v-for="(value, key, index) in person" v-bind:key="value">
                  {{ key }}: {{ value }} ({{ index }})
                </div>
              </li>
              <span v-for="n in 10" v-bind:key="n">{{ n }}</span>
            <hr>
            <div v-for="(ingredient, index) in ingredients" v-bind:key="ingredient">
              <h1>{{ ingredient }}</h1>
              <p>{{ index }}</p>
            </div>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
  export default {
    name: 'Assignment4',
    data: () => ({
      show: true,
      ingredients: ['meat', 'fruit', 'cookies'],
      persons: [
        { name: 'Max', age: 27, color: 'red' },
        { name: 'Anna', age: 'unknown', color: 'blue' }
      ]
    })
  }
</script>
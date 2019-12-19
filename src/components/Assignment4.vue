<template>
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
</template>

<script>
  export default {
    name: 'Assignment4',
    data: () => ({
      show: true
    })
  }
</script>
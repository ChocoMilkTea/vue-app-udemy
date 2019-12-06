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
  </div>
  
</template>

<script>
  export default {
    name: 'Assignment2',
    data: () => ({
      name: 'Thanos'
    })
  }
</script>


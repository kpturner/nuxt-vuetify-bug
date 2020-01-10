<template>
  <div class="container">
    <h1 class="text-center p-8">Nuxt vuetify-module missing classes</h1>
    <v-row align="center">
      <v-col
        class="text-center"
        cols="12"
        sm="4">
        <div class="my-2">
          <v-btn small>Normal</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            small
            color="primary">Primary</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            small
            color="error">Error</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            small
            disabled>Disabled</v-btn>
        </div>
      </v-col>
      <v-col
        class="text-center"
        cols="12"
        sm="4">
        <div class="my-2">
          <v-btn>Normal</v-btn>
        </div>
        <div class="my-2">
          <v-btn color="primary">Primary</v-btn>
        </div>
        <div class="my-2">
          <v-btn color="error">Error</v-btn>
        </div>
        <div class="my-2">
          <v-btn disabled>Disabled</v-btn>
        </div>
      </v-col>
      <v-col
        class="text-center"
        cols="12"
        sm="4">
        <div class="my-2">
          <v-btn large>Normal</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            large
            color="primary">Primary</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            large
            color="error">Error</v-btn>
        </div>
        <div class="my-2">
          <v-btn
            large
            disabled>Disabled</v-btn>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script>


export default {
  asyncData(context) {
    return {
      renderFrom: process.server ? 'server' : 'client'
    }
  },
  data() {
    return { }
  },
  computed: {
    todos() {
     return this.$store.state.todos;
    }
  },
  async fetch({store}) {
   await store.dispatch('todos/index','static');
  },
}
</script>

<style></style>

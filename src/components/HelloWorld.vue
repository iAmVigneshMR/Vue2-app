<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3 mt-10"
          contain
          height="200"
        />
      </v-col>
      <v-col class="mb-1">
        <h1 class="display-2 font-weight-bold mb-3 mt-10">
          Welcome to Vue 2 App
        </h1>
        <v-btn @click="incrementCounter">Add 1</v-btn>
        <h2>{{ counter }}</h2>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import {
  mapState,
  mapMutations,
} from 'vuex';
  export default {
    name: 'HelloWorld',
    data: () => ({
    }),
    computed: {
  ...mapState({
    counter: (state) => state.counter,
  }),
  },
  methods: {
    ...mapMutations([
      'incrementCounter',
    ]),
  },
  }
</script>

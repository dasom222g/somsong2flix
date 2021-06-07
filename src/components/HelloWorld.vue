<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button type="button" @click="getPost">Get data</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: [String, Number],
      required: true,
      default: '',
    },
    exampleArray: {
      type: Array,
      required: false,
      default: () => [],
    },
  },
  methods: {
    async getPost(): Promise<void> {
      const response = await fetch('https://jsonplaceholder.typicode.com/posts')
      const result = await response.json()
      console.log(result)
    },
  },
})
</script>

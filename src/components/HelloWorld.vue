<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button type="button" @click="getPost">Click Here(Get data)</button>
    <div v-for="data in information" :key="data.id">
      <div>{{ data.id }}</div>
      <div>{{ data.title }}</div>
    </div>
  </div>
</template>

<script lang="ts">
// import { PostsType } from '@/types/types'
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'HelloWorld',
  components: {},
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
  data: () => {
    return {
      information: [],
    }
  },
  methods: {
    async getPost() {
      const response = await fetch('https://jsonplaceholder.typicode.com/posts')
      const result = await response.json()
      this.information = result
    },
  },
})
</script>

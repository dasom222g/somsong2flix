<template>
  <div class="home">
    <HelloWorld msg="Welcome to SomSong2flix" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from '@/components/HelloWorld.vue'

export default defineComponent({
  name: 'Home',
  components: {
    HelloWorld,
  },
})
</script>

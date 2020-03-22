<template>
  <div class="container mx-auto">
    <img src="./logo.png">
    <h1>Hello Vue 3!</h1>
    <button @click="inc" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
      Clicked {{ count }} times.
    </button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
}
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>

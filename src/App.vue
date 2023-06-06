<script setup>

import { reactive,computed } from 'vue';

// export default {
  // setup() {
  //   const state = reactive({ count: 0 })

  //   function increment() {
  //     state.count++
  //   }

  //   function decrement() {
  //     state.count--
  //   }

  //   return {
  //     state,
  //     increment,
  //     decrement
  //   }
  // },
// }

const author = reactive({
    name:"firr",
    website:[
      'E-Comers',
      'web-hack',
    ]
  })

  const publishedWeb = computed(() => {
    return author.website.length > 0 ? 'Yes' : 'No' 
  })
</script>

<template>
  <!-- <div>{{ state.count }}</div>
  <button @click="increment">
  PLUS
  </button>
  <button @click="decrement">
  MINUS
  </button> -->
  <div>
    <p>Has published web :</p>
    <span>{{ publishedWeb }}</span>
  </div>
</template>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button {
  margin-right: 10px;
}
</style>

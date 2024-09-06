<template>
  <div>
  <h2>{{count}}</h2>
  <button @click="increment">1000 clicks are you will calm down</button>
  </div>
</template>

<script>
import {ref} from 'vue'; 

export default {
  setup () {
    const count = ref(0);

    function increment() {
      count.value++;
    }

    return {
      count,
      increment
    }
  }
}
</script>

<style>

</style>

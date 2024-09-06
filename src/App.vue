<template>
  <div>
  <h1>{{state.count}}</h1>
  <h2>Click up 500 times and you will calm down</h2>
  <button @click="count_update(true)">Click up</button>
  <h2>If not yet, click back 500 times and you will surely calm down</h2>
  <button @click="count_update(false)">Click down</button>
  
  </div>
</template>

<script>
import {reactive} from 'vue'; 
import './App.css';

export default {
  setup () {
    const state = reactive ({
      count: 0,
    });

    function count_update(increase) {
      if (increase)
        state.count++;
      else 
        state.count--;
    }


    return {
      state,
      count_update
    }
  }
}
</script>

<style>

</style>

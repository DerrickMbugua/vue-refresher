<template>
  <div>
    <h2>Hello {{ state.firstName }}</h2>
    <button @click="state.count++">Count {{ state.count }}</button>
  </div>
</template>
<script>
import { ref,reactive } from "vue";

export default {
  name: "Data",
  setup() {

    const state = reactive({ 
      count: 0,
      firstName: 'Derrick'
     })
    return{
      state
    }
  },
};
</script>
<style scoped>
</style>
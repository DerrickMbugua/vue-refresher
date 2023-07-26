<template>
  <div>
    <h2>Hello {{ firstName }}</h2>
    <button @click="counter++">Count {{ counter }}</button>
  </div>
</template>
<script>
import { ref } from "vue";

export default {
  name: "Data",
  setup() {
    const firstName = ref("Derrick");
    const counter = ref(0);
    return{
      firstName, counter
    }
  },
};
</script>
<style scoped>
</style>
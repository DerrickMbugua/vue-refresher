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
    console.log(firstName);
    console.log(firstName.value);
    const counter = ref(0);
    counter.value += 1;
    return{
      firstName, counter
    }
  },
};
</script>
<style scoped>
</style>
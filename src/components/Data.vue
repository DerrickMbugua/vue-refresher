<template>
  <div>
    <h2>Hello {{ firstName }}</h2>
    <button @click="count++">Count {{ count }}</button>
  </div>
</template>
<script>
import { ref, reactive, toRefs } from "vue";

export default {
  name: "Data",
  setup() {
    const state = reactive({
      count: 0,
      firstName: "Derrick",
    });
    return toRefs(state);
  },
};
</script>
<style scoped>
</style>
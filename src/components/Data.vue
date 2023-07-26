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

    setTimeout(() => {
      state.count = 10;
      state.firstName = "Mwema"
    },2000);

    return toRefs(state);
  }
};
</script>
<style scoped>
</style>
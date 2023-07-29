<template>
  <div>
    <h2>Child B</h2>
    <p>Username is {{ username }}</p>
    <p>Age is {{ myAge }}</p>
    <p>COmposition inject age is {{ age }}</p>
  </div>
</template>
<script>
import { inject } from "vue";
export default {
  name: "ChildB",
  inject: ["username", "myAge"],
  setup() {
    const age = inject("myAge");
    return {
      age,
    };
  },
};
</script>
<style lang="">
</style>
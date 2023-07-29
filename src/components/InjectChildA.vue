<template>
  <div>
    <h2>CHild A</h2>
    <ChildB />
  </div>
</template>
<script>
import ChildB from "./InjectChildB.vue";
export default {
  name: "Child A",
  components: {
    ChildB,
  },
};
</script>
<style lang="">
</style>
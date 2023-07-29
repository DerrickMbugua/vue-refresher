<template>
  <div>
    <button @click="increment">Increment {{ counter }}</button>
  </div>
  <div>
    <input type="text" v-model="firstName" />
  </div>
  <div>
    <input type="text" v-model="lastName" />
    <input type="number" v-model="age" />
  </div>
</template>
<script>
import { ref, watch, reactive, toRefs } from "vue";

export default {
  name: "Watchers",
  setup() {
    const counter = ref(0);
    const firstName = ref("");

    function increment() {
      counter.value++;
    }
    watch(
      [counter, firstName],
      (newValues, oldValues) => {
        // console.log("Counter new value", newValues[0]);
        // console.log("Counter old value", oldValues[0]);
        // console.log("Firstname new value", newValues[1]);
        // console.log("Firstname old value", oldValues[1]);
      },
      {
        immediate: true,
      }
    );

    const state = reactive({
      lastName: "Doe",
      age: 25,
    });

    watch(
      () => {
        return { ...state };
      },
      function (newValues, oldValues) {
        console.log("Lastname new value", newValues.lastName);
        console.log("Lastname old value", oldValues.lastName);
        console.log("Age new value", newValues.age);
        console.log("Age old value", oldValues.age);
      }
    );

    return {
      counter,
      increment,
      firstName,
      ...toRefs(state),
    };
  },
};
</script>
<style scoped>
</style>
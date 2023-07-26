<template>
  <div>
    <h2>Hello {{ name }} {{ last }}</h2>
    <button @click="decrement">Count {{ counter }}</button>
    <button @click="increment">Count {{ count }}</button>
    <button @click="changeName">Change Name</button>
  </div>
</template>

<script>
import { ref, reactive, toRefs } from "vue";

export default {
  name: "Methods",
  setup() {
    const state = reactive({
      name: "Sparta",
      last: "Mwema",
      count: 0
    });

    function changeName(){
      state.name = "Derrick";
      state.last = "Sam"
    }

    function increment(){
      state.count++
    }

    const counter = ref(0);

    function decrement(){
      console.log("CLick button");
      counter.value--;
    }

  

    return {
      name: state.name,
      decrement,
      counter,
      ...toRefs(state),
      increment,
      changeName
    };
  },
};
</script>
<style lang="">
</style>
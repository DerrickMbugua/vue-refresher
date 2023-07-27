<template>
  <div>
    <h2>{{ fullName }}</h2>
    <h2>{{ reactiveFullName }}</h2>
  </div>
</template>
<script>
import { ref, computed, reactive, toRefs } from "vue";
export default {
  name: "Computed",
  setup() {
    const firstName = ref("D");
    const lastName = ref("M");

    const fullName = computed(function () {
      return firstName.value + lastName.value;
    });

    const state = reactive({
      reactiveFirstName: "Sparta",
      reactiveLastName: "Bender",
    });

    const reactiveFullName = computed(function(){
      return state.reactiveFirstName + state.reactiveLastName
    });

   
    return {
      firstName,
      lastName,
      fullName,
      ...toRefs(state),
      reactiveFullName
    };
  },
};
</script>
<style>
</style>
<template>
  <div>
    <input type="text" v-model="heroName"/>
    <input type="text" v-model="firstName"/>
    <input type="text" v-model="lastName"/>
  </div>
</template>
<script>
import { ref, reactive, toRefs } from "vue";

export default {
  name: "Vmodel",
  setup() {
    const heroName = ref("Superman");
    const state = reactive({
      firstName: "Dero",
      lastName: "Mwema",
    });

    return{
      ...toRefs(state),
      heroName
    }
  },
};
</script>
<style lang="">
</style>
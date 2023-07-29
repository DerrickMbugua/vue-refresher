<template>
  <div>
    <h1>Parent</h1>
    <p>My name is {{ name }}</p>
  </div>
  <div>
    <p>My age is {{ age }}</p>
  </div>
  <ChildA />
</template>
<script>
import ChildA from './InjectChildA.vue';
import { ref, provide } from 'vue';
export default {
  name: 'Parent',
  components:{
    ChildA, 
  },
  data(){
    return{
      name: "Sparta"
    }
  },
  provide() {
    return{
      username: this.name
    }    
  },
  setup(){
    const age = ref(26);
    provide('myAge', age.value);

    return{
      age
    }
  }
}
</script>
<style lang="">
  
</style>
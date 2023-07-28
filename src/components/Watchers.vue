<template>
  <div>
    <button @click="count++">Increment {{ count }}</button>
    <button @click="increment">Increment {{ counter }}</button>
  </div>
  <div>
    <input type="text" v-model="firstName" />
  </div>
</template>
<script>
import { ref, watch } from 'vue';

export default {
  name: 'Watchers',
  data() {
    return{
      count : 0,
    }
  },
  watch:{
    count(newValue,oldValue){
      if(newValue === 5){
        alert("High Volume");
      }
    }
  },
  setup(){
    const counter = ref(0);
    const firstName = ref('');

    function increment(){
      counter.value++
    }

    watch([counter, firstName], (newValues, oldValues) => {
     console.log("Counter new value", newValues[0]);
     console.log("Counter old value", oldValues[0]);
     console.log("Firstname new value", newValues[1]);
     console.log("Firstname old value", oldValues[1]);
    },{
      immediate: true
    })
    
    return{
      counter,increment,firstName
    }
  }
 
}
</script>
<style scoped>
  
</style>
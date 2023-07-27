<template>
  <div>
    <h2>{{ fullName }}</h2>
  </div>
</template>
<script>
import {ref, computed} from 'vue';
export default {
  name: 'Computed',
  setup(){
    const firstName = ref('D');
    const lastName = ref('M');

    const fullName = computed(function(){
      return firstName.value + lastName.value;
    });
    return{
      firstName, lastName, fullName
    }
  }

}
</script>
<style>
  
</style>
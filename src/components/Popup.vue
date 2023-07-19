<template>
  <div>
    <h2>Popup Component</h2>
    <button @click="$emit('close')">Close Popup</button>
  </div>
</template>
<script>
export default {
  data(){
    return{
     
    }
  },
  emits: ["close"]
}
</script>
<style>
  
</style>
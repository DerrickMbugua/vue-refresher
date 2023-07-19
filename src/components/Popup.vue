<template>
  <div>
    <h2>Popup Component</h2>
    <input type="text" v-model="name"/>
    <button @click="$emit('close',name)">Close Popup</button>
  </div>
</template>
<script>
export default {
  data(){
    return{
     name: ''
    }
  },
  emits: {
    close(name) {
      if(!name){
        return false;
      }else{
        return true;
      }
    } // event to emit when closing the popup with a value passed as parameter
  }
}
</script>
<style>
  
</style>
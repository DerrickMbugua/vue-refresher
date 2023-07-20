<template>
  <div>
    <h2>Tab C Component</h2>
    <input type="text" v-model="username" />
  </div>
</template>
<script>
export default {
  name: 'Tab C',
  data(){
    return{
      username: ''
    }
  }
}
</script>
<style scoped>
  
</style>
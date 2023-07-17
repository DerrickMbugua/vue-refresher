<template>
  <div>
    Hello {{ message }} {{ likes }}
  </div>
</template>
<script>
export default {
  name: 'Greet',
  data(){
    return{
      
    }
  },
  props: {
    message: String,
    likes: Number
  }
}
</script>
<style>
  
</style>
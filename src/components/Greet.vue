<template>
  <div>
    Hello {{ message }}
  </div>
</template>
<script>
export default {
  name: 'Greet',
  data(){
    return{
      message: 'World!'
    }
  },
  props: [
    'message'
  ]
}
</script>
<style>
  
</style>
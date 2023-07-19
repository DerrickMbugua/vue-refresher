<template>
  <div>
    Hello {{ message }} {{ likes }} {{ isShow }}
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
    message: {
      type: String,
      required: true,
      default: "My Message"
    },
    likes: Number,
    isShow: Boolean
  }
}
</script>
<style>
  
</style>
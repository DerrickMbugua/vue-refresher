<template>
  <div>
    <h1 :style="headerStyling">Components Header</h1>
    <p v-bind="$attrs">Hello {{ name }}</p>
    <p>Hello {{ age }}</p>
  </div>
</template>
<script>
export default {
  name: 'Header',
  data(){
    return{
       headerStyling: {
        color: 'orange',
        fontSize: '20px'
       }
    }
  },
  props: {
    name: String,
    age: Number,  
  },
  inheritAttrs: false
}
</script>
<style>
  
</style>
<template>
  <div>
    <h1 :style="headerStyling">Components Header</h1>
    <p>Hello {{ name }}</p>
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
  props: [
    'name'
  ]
}
</script>
<style>
  
</style>
<template>
  <div>
    <h2>Child Component</h2>
    <input type="text" ref="input" />
  </div>
</template>
<script>
export default {
  name: 'Child',
  mounted(){
    this.$refs.input.focus(); 
  }
}
</script>
<style>
</style>
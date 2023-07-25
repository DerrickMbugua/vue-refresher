<template>
  <div>
    <h2>Child Component</h2>
  </div>
</template>
<script>
export default {
  name: 'Child',
  beforeCreate() {
    console.log("Child before Create") // this will not be executed because it's a function and
  },
  created() {
    console.log('Child Created')
  },
  beforeMount(){
    console.log(`Child before mount`)//this is also an arrow funtion, so
  },
  mounted () {
    console.log('child mounted component');
  },
  beforeUpdate(){
    console.log('Child before update')
  },
  updated(){
    console.log('Child Updated!')
  },
  beforeUnmount(){
    console.log('Child before unmount')
  },
  unmounted(){
    console.log("Child Unmounted")
  }
}
</script>
<style lang="">
</style>
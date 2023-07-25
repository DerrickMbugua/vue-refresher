<template>
  <div>
    <h1>Parent Component</h1>
    <button @click="display = !display">Toggle</button>
    <Child v-show="display" />
  </div>
</template>
<script>
import Child from './Child.vue';
export default {
  name: 'Parent',
  components: {
    Child
  },
  data(){
    return{
      display: true
    }
  },
  beforeCreate() {
    console.log("Parent before Create") 
  },
  created() {
    console.log('Parent Created')
  },
  beforeMount(){
    console.log('Parent before mount')
  },
  mounted () {
    console.log('Parent mounted component');
  },
  beforeUpdate(){
    console.log('Parent before update')
  },
  updated(){
    console.log('Parent Updated!')
  },
  beforeUnmount(){
    console.log('Parent before unmount')
  },
  unmounted(){
    console.log("Parent Unmounted")
  }
}
</script>
<style>
  
</style>
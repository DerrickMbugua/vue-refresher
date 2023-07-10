<template>
<h1 :style="headerStyling">Methods</h1>
<p>{{ add(2,3,4) }}</p>
<p>{{ multipy(5) }}</p>
<p>{{ name }}</p>
<button v-on:click="changeName">Change name</button>
<p>{{ count }}</p>
<button v-on:click="increment">Increment counter</button>
</template>

<script>


export default {
 
  data() {
    return {
      headerStyling: {
        color: 'blue',
        padding: '20px'
      },
      base: 4,
      name: 'Huncho',
      count: 0
    }
  },
  methods: {
    add(a,b,c) {
      return a+b+c
    },
    multipy(num){
      return num * this.base
    },
    increment(){
      this.count++
    },
    changeName(){
      this.name = 'Sparta'
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>

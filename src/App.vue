<template>

  <button @click="count++">{{ count }}</button>
  <h2>Hello {{ name }}</h2>
  <h3 v-text="msg"></h3>

</template>

<script>


export default {
 
  data() {
    return {
      count: 0,
      name: "Derrick",
      msg: "Nmeiva"
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

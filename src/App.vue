<template>
<h1 :style="{
  color: headerColor
}">Conditional Rendering</h1>
<h2 :style="headerStyling">V-if and V-else</h2>
<p v-if="count === 0">The number is zero</p>
<p v-else-if="count < 0">The number is negative</p>
<p v-else-if="count > 0">The number is positive</p>
<p v-else>Not a number</p>
<template v-if="display === true">
<p>One</p>
<p>Two</p>
<p>Three</p>
</template>
</template>

<script>


export default {
 
  data() {
    return {
      count: 'h',
      headerColor: 'orange',
      headerStyling: {
        color: 'black',
        padding: '15px',
        
      },
      display: true
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

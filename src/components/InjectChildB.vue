<template>
  <div>
    <h2>Child B</h2>
    <p>Username is {{ username }}</p>
    <p>Age is {{ myAge }}</p>
  </div>
</template>
<script>
export default {
  name: 'ChildB',
  inject: ["username", "myAge"]
}
</script>
<style lang="">
  
</style>
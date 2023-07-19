<template>
  <div>
    <h2>Component C</h2>
    <h3>COmponent C {{ username }}</h3>
  </div>
</template>
<script>
export default {
  name: 'ComponentC',
  inject: ["username"]
}
</script>
<style>
  
</style>
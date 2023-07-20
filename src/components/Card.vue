<template>
  <div>
    <slot name="header">Header Content</slot>
  </div>
  <div>
    <slot>Default Content</slot>
  </div>
  <div>
    <slot name="footer">Footer Content</slot>
  </div>
 
</template>
<script>
export default {
  name: 'Card'
}
</script>
<style>
  
</style>
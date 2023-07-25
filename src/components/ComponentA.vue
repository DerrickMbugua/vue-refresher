<template>
  <div>
    <h2>Component A</h2>
    <button @click="increment">Count {{ count }}</button>
  </div>
</template>
<script>
import CounterMixin from '../mixin/IncreaseMixin';
export default {
  name: 'ComponentA',
  mixins: [CounterMixin]
}
</script>
<style scoped>
  
</style>
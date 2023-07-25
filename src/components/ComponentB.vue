<template>
  <div>
    <h2>Component B</h2>
    <h3 @mouseover="increment">Hover to Add {{ count }}</h3>
  </div>
</template>
<script>
import CounterMixin from '../mixin/IncreaseMixin';
export default {
  name: 'ComponentB',
  mixins: [CounterMixin]
}
</script>
<style lang="">
  
</style>
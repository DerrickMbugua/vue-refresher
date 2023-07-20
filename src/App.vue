<template>
  <p>App Component</p>
 <Header>
  <template  v-slot:default>
    <p>Header Component</p>
  </template>
 </Header>
 
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: "App",
  components: {
    Header
  },
  data() {
    return {};
  },
  provide() {
    return {};
  },
  methods: {},
};
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
p {
  color: orange;
}

</style>

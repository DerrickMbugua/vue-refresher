<template>
  <!-- <div>
    <h1>App Component</h1>
    <Card></Card>
    <Card>Mapema ndo Best</Card>
    <Card><h2>Mapema ndo Best</h2></Card>
  </div> -->
  <Card>
    <template v-slot:header>
      <h3>Header</h3>
       </template>
       <template v-slot:default>
      <h3>Default</h3>
       </template>
       <template v-slot:footer>
      <h3>Footer</h3>
       </template>
  </Card>

  <List>
    <template v-slot:default="slotProps">
      <h3>{{ slotProps.firstName }} {{ slotProps.lastName }}</h3>
      <h3>{{ slotProps.lastName }} {{ slotProps.firstName }} </h3>
    </template>
  </List>
</template>

<script>
import Card from "./components/Card.vue";
import List from "./components/List.vue";
export default {
  name: "App",
  components: {
    Card,
    List
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

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
abel {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>

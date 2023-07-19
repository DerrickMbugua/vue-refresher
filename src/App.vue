<template>
  <Header id="my-id" name="Mwema" :age="2" />
  <!-- <Greet :message="name" />
  <Greet message="D" :likes="10"/>
  <Greet message="DM" :isShow="isShow"/> -->
<ComponentA />
<p>Name : {{ channel }}</p>
</template>

<script>
import Header from "./components/Header.vue";
import Greet from './components/Greet.vue';
import ComponentA from "./components/ComponentA.vue";

export default {
  name: "App",
  components: {
    Header,
    Greet,
    ComponentA
  },
  data() {
    return {
      name: 'Sparta',
      isShow: true,
      channel : "Mkenyadamu"
    };
  },
  provide() {
    return{
      username: this.channel
    }   
  }
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

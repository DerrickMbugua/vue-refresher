<template>
  <div>
    <h1>App Component</h1>
    <p>Hello {{ name }}</p>
    <button @click="openPopup">Open Popup</button>
    <PopupVue v-show="show" @close="closePopup" />
  </div>
</template>

<script>
import PopupVue from './components/Popup.vue';

export default {
  name: "App",
  components: {
   PopupVue
  },
  data() {
    return {
      show: false,
      name: "Derrick"
    };
  },
  provide() {
    return{
    }   
  },
  methods:{
    openPopup(){
      this.show = true;
    },
    closePopup(name){
      this.show = false;
      this.name = name

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

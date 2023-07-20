<template>
  <div>
    <h1>App Component</h1>
  </div>
  <div style="display: block;">
    <button @click="activeTab = 'TabA'">Tab A</button>
    <button @click="activeTab = 'TabB'">Tab B</button>
    <button @click="activeTab = 'TabC'">Tab C</button>
  </div>
  <!-- <div>
    <TabA v-if="activeTab === 'TabA'"/>
    <TabB v-if="activeTab === 'TabB'"/>
    <TabC v-if="activeTab === 'TabC'"/>
  </div> -->
  <component :is="activeTab" />
</template>

<script>
import TabA from "./components/TabA.vue";
import TabB from "./components/TabB.vue";
import TabC from "./components/TabC.vue";

export default {
  name: "App",
  components: {
    TabA,
    TabB,
    TabC,
  },
  data() {
    return {
     activeTab: 'TabA'
    };
  },
  provide() {
    return {};
  },
  methods:{
  
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
</style>

<template>
  <p :style="headingStyling">Watchers</p>
  <h2>Current Volume - {{ volume }}</h2>
  <div>
    <button @click="increaseVolume">Increase</button>
    <button @click="decreaseVolume">Decrease</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      headingStyling: {
        color: "orange",
      },
      volume: 0,
    };
  },
  methods: {
    increaseVolume(){
      return this.volume += 2;
    },
    decreaseVolume(){
      return this.volume -= 2;
    }
  },
  computed: {},
  watch: {
    volume(newVolume, oldVolume){
      if(newVolume > oldVolume && newVolume == 10){
        alert('High Volume!!')
      }
    }
  },
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

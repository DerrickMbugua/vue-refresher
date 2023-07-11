<template>
  <p :style="headingStyling">{{ firstName }} {{ lastName }}</p>
  <p>{{ fullName }}</p>
  <template v-for="item in items" :key="item.id">
    <p v-if="item.price > 9999">{{ item.title }}</p>
  </template>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "D",
      lastName: "M",
      headingStyling: {
        color: "orange",
      },
      items: [
        {
          id: 1,
          title: "TV",
          price: 10000,
        },
        {
          id: 2,
          title: "IPhone",
          price: 1000,
        },
        {
          id: 3,
          title: 'Watch',
          price: 100
        }
      ],
    };
  },
  methods: {},
  computed: {
    fullName() {
      return this.firstName + " " + this.lastName;
    },
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

<template>
  <p :style="headingStyling">{{ firstName }} {{ lastName }}</p>
  <p>{{ fullName }}</p>
  <button @click="changeFullName">Change fullName</button>
  <template v-for="item in items" :key="item.id">
    <!-- <p v-if="item.price > 9999">{{ item.title }}</p> -->
    <p>{{ item.title }} {{ item.price }}</p>
  </template>
  <p>Total Price of items<strong>{{ totalPrice }}</strong></p>
  <button @click="addItem">Add Item</button>
  <p v-for="item in expensiveItem" :key="item.id">{{ item.title }}</p>
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
  methods: {
    addItem(){
      // Create a new item object
      const newItem = {
        id: 4,
        title: 'Android',
        price: 10
      };

      this.items.push(newItem);
      console.log('Add Item');
    },
    changeFullName(){
      this.fullName = 'Mary Jane';
    }
  },
  computed: {
    fullName: {
      get(){
        return this.firstName + " " + this.lastName;
      },
      set(value){
        const names = value.split(' ');
        this.firstName = names[0];
        this.lastName = names[1];
      }
    },
    totalPrice() {
      return this.items.reduce((total, item) => total + item.price, 0);
    },
    expensiveItem(){
      return this.items.filter((item) => item.price > 100);
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

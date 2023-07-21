<template>
  <div>
    <form @submit.prevent="createPost">
      <div>
        <label>Title: </label>
        <input type="text" v-model="formData.title" />
      </div>
      <div>
        <label>Body: </label>
        <input type="text" v-model="formData.body" />
      </div>
      <div>
        <label>User ID: </label>
        <input type="number" v-model="formData.userId" />
      </div>
      <div>
        <button>Save</button>
      </div>
    </form>
  </div>
</template>
<script>
import axios from 'axios';
export default { 
  data() {
    return {
      formData: {
        title: "",
        body: "",
        userId: ""
      },
    };
  },
  methods: {
    createPost() {
      axios.post("https://jsonplaceholder.typicode.com/posts", this.formData)
      .then((response) => {
        console.log(response.data);
      })
      .catch((error) => {
        console.log(error);
      });
    },
  },
};
</script>
<style lang="">
</style>
<template>
  <div>
    <form @submit.prevent="submitForm">
      <div>
        <label for="userId">User ID</label>
        <input type="number" id="userId" v-model="formData.userId" />
      </div>
      <div>
        <label for="title">Title</label>
        <input type="text" id="title" v-model="formData.title" />
      </div>
      <div>
        <label for="body">Body</label>
        <textarea v-model="formData.body"></textarea>
      </div>
      <div>
        <button>Submit</button>
      </div>
    </form>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  name: 'CreatePost',
  data(){
    return{
      formData: {
        userId: '',
        title: '',
        body: ''
      }
    }
  },
  methods:{
    submitForm(){
      console.log(this.formData);
      axios.post("https://jsonplaceholder.typicode.com/posts", this.formData)
      .then((response) => {
        console.log(response.data)
      })
      .catch((error) => {
        console.log(error.message)
      });
    }
  }
}
</script>
<style>
  
</style>
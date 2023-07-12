<template>
  <div>
    <button @click="getPosts">Load Posts</button>
  </div>
  <p v-if="errorMsg">{{ errorMsg }}</p>
  <template v-for="post in posts" :key="post.id"> 
    <p>{{ post.title }}</p>
  </template>
</template>
<script>
import axios from 'axios'
export default {

  name: 'PostList',
  data(){
    return{
      posts: [],
      errorMsg: ''
    }
  },
  methods: {
    getPosts(){
      axios.get("https://jsonplaceholder.typicode.com/posts")
      .then((response) => {
        console.log(response.data)
        this.posts = response.data
      })
      .catch((error) => {
        console.log(error)
        this.errorMsg = error.message
      })
    }
  }
}
</script>
<style>
  
</style>
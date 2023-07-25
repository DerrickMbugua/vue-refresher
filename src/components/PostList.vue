<template>
  <div>
    <button @click="getPosts">Load Posts</button>
  </div>
  <div v-for="post in posts" :key="post.id">
    <p>{{ post.id }}</p>
    <p>{{ post.title }}</p>
  </div>
</template>
<script>
import axios from "axios";

export default {
  name: "PostList",
  data() {
    return {
      posts: [],
    };
  },
  created() {
    this.getPosts()
  },
  methods: {
    getPosts() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((response) => {
          console.log(response.data);
          this.posts = response.data;
        })
        .catch((error) => {
          console.log(error.message);
        });
    },
  },
 
};
</script>
<style scoped>
</style>
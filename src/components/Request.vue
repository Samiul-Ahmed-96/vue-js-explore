<template>
  <hr />
  <h2>Get Request</h2>
  <hr />
  <div>
    <button @click="loadData">Load data</button>
  </div>
  <div class="posts">
    <div v-for="post in posts" :key="post.id" class="post">
      <h3>{{ post.id }}</h3>
      <h4>{{ post?.title }}</h4>
    </div>
  </div>
  <hr />
  <h2>Post Request</h2>
  <hr />
</template>

<script>
import axios from "axios";
export default {
  name: "request- area",
  data() {
    return {
      posts: [],
    };
  },
  methods: {
    loadData() {
      axios
        .get("https://jsonplaceholder.typicode.com/posts")
        .then((res) => {
          console.log(res.data);
          this.posts = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style scoped></style>

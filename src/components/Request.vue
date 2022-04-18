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
  <div class="post">
    <form @submit.prevent="formSubmit">
      <div>
        <label for="id">Your Id</label>
        <br />
        <input id="id" type="text" v-model="formData.userId" />
      </div>
      <div>
        <label for="name">Your Name</label>
        <br />
        <input id="name" type="text" v-model="formData.name" />
      </div>
      <div>
        <label for="message">Your Message</label>
        <br />
        <input id="message" type="text" v-model="formData.body" />
      </div>
      <button>Submit Form</button>
    </form>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "request- area",
  //   created() {
  //     this.loadData();
  //   },
  data() {
    return {
      posts: [],
      formData: {
        name: "",
        userId: "",
        body: "",
      },
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
    formSubmit() {
      axios
        .post("https://jsonplaceholder.typicode.com/posts", this.formData)
        .then((res) => console.log(res.data))
        .catch((err) => console.log(err));
    },
  },
};
</script>

<style scoped></style>

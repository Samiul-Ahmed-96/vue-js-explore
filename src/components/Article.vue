<template>
  <h2>Article - Props</h2>
  <h3>{{ likes }}</h3>
  <h3>{{ title }}</h3>
  <h3>isPublished - {{ isPublished === true ? "Yes" : "No" }}</h3>
</template>

<script>
export default {
  name: "Article-props",
  props: {
    title: String,
    likes: Number,
    isPublished: Boolean,
  },
  data() {
    return {};
  },
};
</script>

<style scoped></style>

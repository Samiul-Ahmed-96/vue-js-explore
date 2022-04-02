<template>
  <hr />
  <h2>Binding Text</h2>
  <hr />
  <h5>Explore {{ name }}</h5>
  <hr />
  <h2>V-text</h2>
  <hr />
  <div v-text="myOffice"></div>
  <hr />
  <h2>V-html</h2>
  <hr />
  <div v-html="myOfficeTwo"></div>
</template>

<script>
export default {
  name: "Binding-vue",
  data() {
    return {
      name: "Hello Vue",
      myOffice: "Bangladesh Software Solution",
      myOfficeTwo: "<b>Bangladesh Software Solution</b>",
    };
  },
};
</script>

<style scoped></style>

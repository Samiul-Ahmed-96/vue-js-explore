<template>
  <div>
    <h1>Hello from home {{ 10 + 10 }}</h1>
    <h2>{{ name }}</h2>
    <h2>{{ getName("Sakib") }}</h2>
    <h3>{{ getUser().name }}</h3>
    <h3>{{ getUser().email }}</h3>
  </div>
</template>

<script>
export default {
  name: "Home-Page",
  data() {
    return {
      name: "Anik",
      email: "kavin@gma.com",
    };
  },
  methods: {
    getName(name) {
      return name;
    },
    getUser() {
      return {
        name: "Kavin",
        email: this.email,
      };
    },
  },
};
</script>

<style scoped>
h1 {
  color: rgb(18, 109, 79);
}
</style>

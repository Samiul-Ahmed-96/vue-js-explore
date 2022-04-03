<template>
  <Binding />
  <Methods />
</template>

<script>
import Binding from "./components/Binding.vue";
import Methods from "./components/Methods.vue";
export default {
  name: "App",
  components: {
    Binding,
    Methods,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>

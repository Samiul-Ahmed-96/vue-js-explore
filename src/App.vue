<template>
  <Binding />
</template>

<script>
import Binding from "./components/Binding.vue";
export default {
  name: "App",
  components: {
    Binding,
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

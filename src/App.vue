<template>
  <Binding />
  <Methods />
  <EventHandling />
</template>

<script>
import Binding from "./components/Binding.vue";
import Methods from "./components/Methods.vue";
import EventHandling from "./components/EventHandling.vue";

export default {
  name: "App",
  components: {
    Binding,
    Methods,
    EventHandling,
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

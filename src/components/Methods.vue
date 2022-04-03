<template>
  <hr />
  <h2>Methods</h2>
  <hr />
  <h3>{{ counter }}</h3>
  <button @click="increase(5)">Increase</button>
  <button @click="decrease(5)">Decrease</button>
</template>

<script>
export default {
  name: "Methods-vue",
  data() {
    return {
      counter: 0,
      disabled: false,
    };
  },
  methods: {
    increase(num) {
      return (this.counter = this.counter + num);
    },
    decrease(num) {
      return (this.counter -= num);
    },
  },
};
</script>

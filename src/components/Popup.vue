<template>
  <div>
    <h2>Popup Here</h2>
    <button @click="$emit('close')">Close</button>
  </div>
</template>

<script>
export default {
  name: "Popup-Compo",
  emits: ["close"],

  data() {
    return {};
  },
};
</script>

<style scoped></style>

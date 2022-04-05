<template>
  <hr />
  <h2>Slots</h2>
  <hr />
  <div>
    <div class="card">
      <div class="header"><slot name="header"></slot></div>
      <div class="default"><slot></slot></div>
      <div class="footer"><slot name="footer"></slot></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "slots-area",
};
</script>

<style scoped>
.card {
  background: #333;
  color: #fff;
  padding: 20px;
  margin: 10px;
  display: inline-block;
}
.card img {
  width: 300px;
}
</style>

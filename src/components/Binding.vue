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
  <hr />
  <h2>V-bind</h2>
  <hr />
  <div v-bind:id="divId">V-bind</div>
  <hr />
  <h2>V-bind-attributes</h2>
  <hr />
  <button v-bind:disabled="isDisabled">Bind Boolean-True</button>
  <br />
  <br />
  <button v-bind:disabled="isDisabled === false">Bind Boolean-False</button>
  <hr />
  <h2>V-bind-classes</h2>
  <hr />
  <div class="normal-class" v-bind:class="status">Status</div>
  <br />
  <div v-bind:class="isSold ? 'sold' : 'available'">Soldout Movie</div>
</template>

<script>
export default {
  name: "Binding-vue",
  data() {
    return {
      name: "Hello Vue",
      myOffice: "Bangladesh Software Solution",
      myOfficeTwo: "<b>Bangladesh Software Solution</b>",
      divId: "v-bind",
      isDisabled: true,
      status: "dynamic-class",
      isSold: false,
    };
  },
};
</script>

<style scoped>
.sold {
  color: red;
}
.available {
  color: green;
}
</style>

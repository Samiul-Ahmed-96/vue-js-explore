<template>
  <div class="part-one">
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
    <hr />
    <h2>V-bind-style-inline</h2>
    <hr />
    <div
      v-bind:style="{
        color: vBindColor,
        'font-size': vBindSize + 'px',
        background: 'yellow',
      }"
    >
      Hello from v-bind-styles
    </div>
    <br />
    <div v-bind:style="styleObj">Style object</div>
  </div>
  <div class="part-two">
    <br /><br /><br />
    <hr />
    <h2>Conditional Rendering</h2>
    <hr />
    <h3 v-if="number === 0">The is v-if</h3>
    <h3 v-else-if="number < 0">The is v-else-if</h3>
    <h3 v-else>The is else</h3>
    <h3 v-show="showName">V-show</h3>
  </div>
  <div class="part-">
    <br /><br />
    <hr />
    <h2>List Rendering</h2>
    <hr />
    <h3 v-for="name in names" :key="name">{{ name }}</h3>
    <h2>Render Objects of array</h2>
    <div v-for="actor in actors" :key="actor">
      <h3>{{ actor.name }}</h3>
      <h3 v-for="color in actor.favColor" :key="color">
        {{ color }}
      </h3>
    </div>
  </div>
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
      vBindColor: "#444",
      vBindSize: 50,
      styleObj: {
        fontSize: "50px",
        border: "3px solid #444",
      },
      number: 6,
      showName: true,
      names: ["Shakib", "Prova", "Tamim"],
      actors: [
        { name: "AAAAA", favColor: ["Black", "Blue"] },
        { name: "VVVVV", favColor: ["Yellow", "Red"] },
      ],
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
h2 {
  color: rgb(156, 36, 241);
  font-size: 40px;
  font-style: italic;
}
</style>

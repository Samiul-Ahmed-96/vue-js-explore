<template>
  <hr />
  <h2>Form Handling</h2>
  <hr />
  <pre>
      {{ JSON.stringify(formValues, null, 2) }}
  </pre>
  <from>
    <div>
      <label for="name">Name</label>
      <br />
      <input v-model="formValues.name" type="text" id="name" />
      <br />
      <label for="password">Password</label>
      <br />
      <input v-model="formValues.password" type="password" id="password" />
    </div>
  </from>
</template>
<script>
export default {
  name: "Event-handling",
  data() {
    return {
      formValues: {
        name: "",
        password: "",
      },
    };
  },
};
</script>

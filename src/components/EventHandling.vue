<template>
  <hr />
  <h2>Form Handling - Modifiers (trim,number,lazy)</h2>
  <hr />
  <!-- Form Handling -->
  <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
  </div>
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <br />
      <input type="text" id="name" v-model.trim="formValues.name" />
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <br />
      <textarea id="profile" v-model="formValues.profileSummary" />
    </div>
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValues.country">
        <option value="">Select a country</option>
        <option value="Bangladesh">Bangladesh</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>
    <br />
    <div>
      <label for="job-location">Job location</label>
      <br />
      <select id="job-location" v-model="formValues.jobLocation" multiple>
        <option value="Bangladesh">Bangladesh</option>
        <option value="vietnam">Vietnam</option>
        <option value="singapore">Singapore</option>
      </select>
    </div>
    <br />
    <div>
      <input
        id="remoteWork"
        type="checkbox"
        v-model="formValues.remoteWork"
        true-value="yes"
        false-value="no"
      />
      <label for="remoteWork">Open to remote work?</label>
    </div>
    <br />
    <div>
      <label>Skill set</label>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValues.skillSet"
      />
      <label for="html">HTML</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValues.skillSet"
      />
      <label for="css">CSS</label>
      <input
        type="checkbox"
        id="javascript"
        value="javascript"
        v-model="formValues.skillSet"
      />
      <label for="javascript">JavaScript</label>
    </div>
    <div>
      <br />
      <label>Years of Experience</label>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.yearsOfExperience"
      />
      <label for="0-2">0-2</label>
      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.yearsOfExperience"
      />
      <label for="3-5">3-5</label>
      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.yearsOfExperience"
      />
      <label for="6-10">5-10</label>
      <input
        type="radio"
        id="10+"
        value="10+"
        v-model="formValues.yearsOfExperience"
      />
      <label for="10+">10+</label>
    </div>
    <br />
    <div>
      <label for="age">Age</label>
      <input type="number" id="age" v-model.number="formValues.age" />
    </div>
    <br />
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>
<script>
export default {
  name: "Event-handling",
  data() {
    return {
      formValues: {
        name: "",
        profileSummary: "",
        country: "",
        jobLocation: [],
        remoteWork: "no",
        skillSet: [],
        yearsOfExperience: "",
        age: null,
      },
    };
  },
  methods: {
    submitForm(event) {
      event.preventDefault();
      console.log(this.formValues);
    },
  },
};
</script>

<template>
  <h1>This is a simple form in vue js</h1>
  <div v-for="item in error" v-bind:key="item">{{ item }} cannot be empty</div>
  <form @submit.prevent="getFormData">
    <label for="name">Name</label>
    <input type="text" name="name" id="name" v-model="formdata.name" />
    <br /><br /><br />
    <label for="email">Email</label>
    <input type="text" name="email" id="email" v-model="formdata.email" />
    <br /><br /><br />
    <label for="Age">Age</label>
    <input type="text" name="Age" id="Age" v-model="formdata.Age" />
    <br />
    <select name="country" id="country" v-model="formdata.counrtry" multiple>
      <option value="china">china</option>
      <option value="India">India</option>
      <option value="Usa">Usa</option>
    </select>

    <h2>Technology Stack</h2>
    <label for="React">React</label>
    <input
      type="checkbox"
      name="React"
      value="React"
      id="React"
      v-model="formdata.technology"
    />

    <label for="vue">vue</label>
    <input
      type="checkbox"
      name="vue"
      value="vue"
      id="vue"
      v-model="formdata.technology"
    />

    <label for="Angular">Angular</label>
    <input
      type="checkbox"
      name="Angular"
      id="Angular"
      value="Angular"
      v-model="formdata.technology"
    />
    <br />
    <label for="male">Male</label>
    <input
      type="radio"
      name="gender"
      id="male"
      value="male"
      v-model="formdata.gender"
    />

    <label for="Female">Female</label>
    <input
      type="radio"
      name="gender"
      id="Female"
      value="female"
      v-model="formdata.gender"
    />

    <br /><br /><br />

    <button>Submit</button>

    <div class="json-cont">
      <pre v-if="btntoggler">JSON PREVIEW :{{ formdata }}</pre>
    </div>
  </form>
</template>

<script>
export default {
  name: "SimpleForm",
  data() {
    return {
      Array: [],
      formdata: {
        name: null,
        email: null,
        Age: null,

        counrtry: [],
        technology: [],
        gender: null,
      },
      btntoggler: false,
      error: [],
    };
  },
  methods: {
    getFormData() {
      console.log(this.formdata);
      this.error = [];

      for (const item in this.formdata) {
        if (this.formdata[item] === null || this.formdata[item].length === 0) {
          this.error.push(item);
        }
      }
      console.log(this.error);

      if (this.error.length == 0) {
        this.btntoggler = true;
      } else {
        this.btntoggler = false;
      }
    },
  },
};
</script>
<style scoped>
.json-cont {
  position: absolute;
  top: 50px;
  left: 50%;
  font-size: 1.2rem;
}
</style>

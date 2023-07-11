<template>
  <h1 :style="headerStyling">Form Handling</h1>
  <form @submit="formHandling">
    <p>{{ formValues.name }}</p>
    <p>{{ formValues.message }}</p>
    <p>{{ formValues.selected }}</p>
    <p>{{ formValues.multiple }}</p>
    <div>
      <label for="name">Name</label>
      <input type="text" v-model="formValues.name" />
    </div>
    <div>
      <label for="message">Message</label>
      <textarea
        v-model="formValues.message"
        placeholder="add multiple lines"
      ></textarea>
    </div>
    <div>
      <label for="message">Select</label>
      <select v-model="formValues.selected">
        <option disabled value="">Please select one</option>
        <option value="A">A</option>
        <option value="B">B</option>
        <option value="C">C</option>
      </select>
    </div>
    <div>
      <label for="message">Select Multiple</label>
      <select multiple v-model="formValues.multiple">
        <option value="A">A</option>
        <option value="B">B</option>
        <option value="C">C</option>
      </select>
    </div>
    <div>
      <input type="checkbox" id="checkbox" v-model="formValues.checked" />
      <label for="checkbox">{{ formValues.checked }}</label>
    </div>
    <div>Picked: {{ formValues.picked }}</div>

    <input type="radio" id="one" value="One" v-model="formValues.picked" />
    <label for="one">One</label>

    <input type="radio" id="two" value="Two" v-model="formValues.picked" />
    <label for="two">Two</label>
    <div>
      <button>Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      headerStyling: {
        color: "blue",
        fontSize: "30px",
      },
      formValues: {
        name: "",
        message: "",
        selected: "",
        multiple: [],
        checked: '',
        picked: ''
      },
    };
  },
  methods: {
    formHandling(event){
      event.preventDefault()
      console.log('Form Values', this.formValues)
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
abel {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}
input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.42857143;
  color: #555;
  background-color: #fff;
  background-image: none;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>

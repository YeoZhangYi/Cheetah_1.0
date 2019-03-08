<template>
  <div class="home_page">
    <img
      src="https://uploads.codesandbox.io/uploads/user/0ea490f3-9d76-4d04-942e-cf1ed72b5a0b/yJwV-nudsmodslogo.png"
      alt="Alternative Text"
    />
    <br /><br />
    <li>
      <b-form @submit="onSubmit">
        <b-form-input
          id="enteredModuleCode"
          type="text"
          v-model="form.text"
          required
          placeholder="Enter module code"
        />
        <b-button
          type="submit"
          variant="primary"
          @click="modalShow = !modalShow;"
          >Submit</b-button
        >
      </b-form>
    </li>
    <br /><br />
    <h2>View popular modules by:</h2>
    <br /><br />
    <ul>
      <li>
        <input type="button" />
        <input type="button" value="Faculty" class="button2" /> <br /><br />
        <h5>
          Categorised according to modules completed by seniors in your faculty
        </h5>
        <p>
          Find out which year you should be clearing certain modules based on
          what your seniors did
        </p>
      </li>
      <li>
        <input type="button" />
        <input type="button" value="Module Type" class="button2" /> <br /><br />
        <h5>
          Categorised according to module type (e.g. GE mods, lanuguage mods)
        </h5>
        <p>
          Find out which are popular GE modules to take basd on your ideal
          workload requirements
        </p>
      </li>
      <li>
        <input type="button" />
        <input type="button" value="Industry" class="button2" /> <br /><br />
        <h5>
          Categorised according to modules completed by graduates in specific
          industries
        </h5>
        <p>
          Find out which modules will teach you useful knowledge/ skills to work
          in your ideal industry
        </p>
      </li>
    </ul>

    <br /><br /><br />
    <footer />
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue";
export default {
  data() {
    return {
      form: {},
      modalShow: false
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
    }
  },
  name: "home",
  components: {
    Footer
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img {
  width: 300px;
  height: 80px;
}
h3 {
  margin: 40px 0 0;
}
h2 {
  color: #ee7230;
}
h5 {
  color: #023d7c;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 20px;
  width: 260px;
}

p {
  font-size: 12px;
}

input[type="button"].button2 {
  height: 120px;
  width: 240px;
  background-color: #023d7c;
  color: white;
  font-size: 32px;
}

a {
  color: #42b983;
}
</style>

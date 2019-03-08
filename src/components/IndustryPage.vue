<template>
  <div class="industry_page">
    <img
      src="https://uploads.codesandbox.io/uploads/user/0ea490f3-9d76-4d04-942e-cf1ed72b5a0b/iwd_-industrypic.png"
      alt="Alternative Text"
    />
    <br /><br />
    <p>
      Discover modules recently employed graduates took while they were
      studying.
    </p>
    <p>
      This information can serve as a useful guideline of skills and knowledge
      that would be helpful for a certain industry.
    </p>

    <br /><br />
    <div id="container">
      <div id="contain">
        <h5>Category:</h5>
        <select>
          <option value="volvo">Volvo</option>
          <option value="saab">Saab</option>
          <option value="mercedes">Mercedes</option>
          <option value="audi">Audi</option>
        </select>
      </div>
    </div>
    <br /><br />
    <table class="table table-striped">
      <thead>
        <tr>
          <th>Rank</th>
          <th>Module</th>
          <th>Total Enrolment</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Jill</td>
          <td>Smith</td>
          <td>50</td>
        </tr>
      </tbody>
    </table>
    <br /><br /><br />
    <footer />
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue";
import { module_enrolment } from "../firebase";
export default {
  name: "industry",
  data() {
    return {
      items: []
    };
  },
  firebase: {
    items: module_enrolment
  },
  components: {
    Footer
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
p {
  margin-left: 200px;
  margin-right: 200px;
  margin-top: 0px;
  margin-bottom: 0px;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
table {
  width: 850px;
  padding: 0px;
  display: table;
  margin-left: auto;
  margin-right: auto;
}

#contain {
  display: inline-block;
  width: 250px;
}
h5 {
  color: #105da5;
}
th {
  font-size: 12px;
}
</style>

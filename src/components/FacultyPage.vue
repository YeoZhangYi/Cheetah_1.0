<template>
  <div class="batch_page">
    <img
      src="https://uploads.codesandbox.io/uploads/user/0ea490f3-9d76-4d04-942e-cf1ed72b5a0b/vbmV-modulepic.png"
      alt="Alternative Text"
    />
    <br /><br />

    <p>Discover modules based on your module types.</p>
    <p>
      Find out what other chose for their Programme Electives, or/ and find out
      more about popular GE mods.
    </p>

    <br /><br />
    <div id="container">
      <div id="contain">
        <h5>Faculty / Major:</h5>
        <select>
          <option value="volvo">Volvo</option>
          <option value="saab">Saab</option>
          <option value="mercedes">Mercedes</option>
          <option value="audi">Audi</option>
        </select>
      </div>
      <div id="contain">
        <h5>Category:</h5>
        <select>
          <option value="volvo">Volvo</option>
          <option value="saab">Saab</option>
          <option value="mercedes">Mercedes</option>
          <option value="audi">Audi</option>
        </select>
      </div>
      <div id="contain">
        <h5>Workload:</h5>
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
          <th>Filtered Enrolment</th>
          <th>Filtered Enrolment(%)</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item of items" :key="item['.key']">
          <td>{{ item.module_code }}</td>
        </tr>
      </tbody>
    </table>
    <br /><br /><br />
    <footer />
  </div>
</template>

<script>
import Footer from "@/components/Footer.vue";
export default {
  name: "batch",
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

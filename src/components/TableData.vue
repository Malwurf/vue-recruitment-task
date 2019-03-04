<template>
  <div class="hello">
    <h1>{{ msg }}</h1>

    <table>
      <thead>
      <tr>
        <th>Name</th>
        <th>Hash</th>
        <th>Status</th>
        <th>Balance</th>
      </tr>
      </thead>
      <tbody>
        <tr v-for="item in jsonData" v-bind:key="item.id">
          <td>{{ item.name.first }}</td>
          <td>{{ item.hash }}</td>
          <td>{{ item.transfered }}</td>
          <td>{{ item.balance }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import jsonData from '../assets/data.json';

export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data: function() {
    return {
      jsonData: jsonData
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

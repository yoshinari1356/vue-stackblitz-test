<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br />
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >.
    </p>
    <h3>list</h3>
    <ul>
      <li v-for="item in list">
        <a href="https://vuejs.org" target="_blank" rel="noopener">{{
          item.title
        }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
import ListJson from "../../assets/json/list.json";
export default {
  name: "NEW",
  props: {
    msg: String
  },
  data() {
    return {
      list: []
    };
  },
  created() {
    this.list = JSON.parse(JSON.stringify(ListJson));
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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

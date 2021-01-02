<template>
  <div id="app">
    <span>page: {{ page }}</span>
    <button @click="clickbtn">クリック</button>
    <HelloWorld msg="HelloWorld" v-if="page == 0" />
    <New msg="new xxx" v-if="page == 1" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import New from "./components/new.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    New
  },
  data() {
    return {
      page: 1
    };
  },
  methods: {
    clickbtn(e) {
      if (this.page == 1) {
        this.page = 0;
      } else {
        this.page = 1;
      }
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

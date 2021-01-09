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
import Tile from "./components/tile.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    New,
    Tile
  },
  data() {
    return {
      page: 1,
      max_page: 2
    };
  },
  methods: {
    clickbtn(e) {
      if (this.page == this.max_page) {
        this.page = 0;
      } else {
        this.page += 1;
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
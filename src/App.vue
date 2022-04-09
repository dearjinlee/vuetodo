<template>
  <div id="app">
    <Header />
    <Todolist />
	<Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Todolist from './components/Todolist.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
	Todolist,
	Footer
  },
  data:function() {
	  return {
		  hello:"a",
	  }
  },
  methods: {
	  // childCall() {
	  // console.log("childCall")
	  // //this.$emit('hello', "b")
	  // }
	  childCall(val) {
		  console.log(val)
		  this.hello = val
	   }
  }
}
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

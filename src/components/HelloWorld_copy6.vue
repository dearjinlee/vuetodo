<template>
  <div id="app-4">
	  <p>{{ message }} </p>
	  <button v-on:click="reverseMessage">메세지 뒤집기</button>
  </div>
</template>

<script>
var code = {
	name:'a', age:'10',
};
export default {
  el: '#example-2',
  name: 'HelloWorld',
  data: function() {
	return {
		message: '안녕~ vue.js 안녕하세요~ 진짜루~'
	}
  },
  methods: {
	  reverseMessage() {
		  console.log("reverseMessage")
		  this.message = this.message.split('').reverse().join('');
	  }
  }
}
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
.name1 {
	background-color: red;
}
.red {
	background-color: red;
}
.blue {
	background-color: blue;
}
.green {
	background-color: green;
}
.yellow {
	background-color: yellow;
}
</style>

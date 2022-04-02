<template>
  <div id="app-4">
	  <input v-mode="a"></input>
	  <input v-mode="n"></input>
	  <button v-on:click="add">Add</button>
	  <button v-on:click="sub">Sub</button>
	  <p>위 버튼을 클릭한 횟수는 {{ result }} 번 입니다.</p>
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
		a : 0,
		b : 0,
		result : 0
	}
  },
  methods: {
	  add: function() {
		  console.log("add")
		  //this.result = this.a + this.b
		  this.result = this.a + this.b
	  },
	  sub: function() {
		  console.log("sub")
		  //this.result = this.a - this.b
		  this.result = this.a - this.b
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

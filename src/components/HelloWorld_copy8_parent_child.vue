<template>
	  <button @click="emitCall">값을 바꿔주세요</button>
</template>

<script>
var code = {
	name:'a', age:'10',
};
export default {
  el: '#example-2',
  name: 'HelloWorld',
  props: ['prop'],
  data: function() {
	return {
	}
  },
  methods: {
	  emitCall() {
		  console.log("emitCall")
		  this.$emit('hello', "b") // to parent
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

<template>
  <div id="app-4">
	  <button v-on:click="counter += 1">Add 1</button>
	  <p>위 버튼을 클릭한 횟수는 {{ counter }} 번 입니다.</p>
	  <p>{{ name }}님의 나이는 {{ age }} 입니다.</p>
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
		name : "Jin",
		age : 20,
		counter: 0
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

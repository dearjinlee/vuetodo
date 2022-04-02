<template>
  <div class="hello">
	<ul id="example-2">
		<li v-for="(item, index) in items">
			{{ parentMessage }} - {{ index }} - {{ item.message }}
		</li>
	</ul>
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
		parentMessage: 'Parent',
		items: [
			{ message: 'Foo' },
			{ message: 'Bar' }
		],
	}
  },
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

<template>
  <div class="hello">
	<!-- <input type="text" v-model="msg" /> -->
	<!-- <h3 v-if="flag"> flag 값이 true 일때만 나옵니다. </h3> -->
	
	<ul v-for="item in items">
		<!-- <li> {{ item.name}} </li> -->
		<li> {{ item.name + " 의 가격은 " + item.price + "입니다" }} </li>
	</ul>
  </div>
</template>

<script>
var code = {
	name:'a', age:'10',
};
export default {
  name: 'HelloWorld',
  data: function() {
	return {
		msg: 'vue.js입니다.',
		flag: true,
		items: [
			{name:'피자', price:'23000'},
			{name:'햄버거', price:'6000'},
			{name:'떡볶이', price:'10000'},
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

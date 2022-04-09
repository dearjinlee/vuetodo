<template>
	<div>
		
    <!-- main.todo -->
    <main class="todo">
        <div class="container">
            <h1>To - Do List</h1>

            <!-- ul.list_add -->
			<!--
            <ul class="list_add">
                <li class="list_add_tit"><p>등록 하기</p></li>
                <li><p><input type="text"><button>등 록</button></p></li>
            </ul>
			-->
			<TodoInput @addTodo="addTodo" />
            <!--// ul.list_add -->

            <!-- ul.todo_list -->
            <ul class="todo_list">
                <li class="todo_list_tit"><p>할 일</p></li>
                <li><p> {{ remaining }} / {{ todolist.length }} 건 처리 </p></li>

                <li class="del_btn" v-for="(item,index) in todolist" :key="index">
                    <p :class="{doneStyle:item.done}"><input type="checkbox" name="check1" v-model="item.done">{{ item.todo }}</p>
                    <ul class="todo_list_btn">
                        <li><button @click="updateTodo">수 정</button></li>
                        <li><button @click="subTodo(index)">삭 제</button></li>
                    </ul>
                </li>

            </ul>
            <!--// ul.todo_list -->

        </div>
    </main>
    <!--// main.todo -->
	</div>
</template>

<script>
import TodoInput from './TodoInput.vue'

export default {
  name: 'todolist',
  components: {
	  TodoInput,
  },
  data: function() {
	return {
		todolist:[
			{done:false, todo:"vue.js 공부하기"},
			{done:false, todo:"독서 2p 이상"},
			{done:false, todo:"보안 과제하기"},
			{done:false, todo:"9시 스터디하기"},
			{done:true, todo:"과제 채점"},
		]
	}
  },
  computed:{
	  remaining() {
		  /*
		  this.todolist.filter(function(val){
			  console.log(val);
		  })
		  return 0;
		  */
		  return this.todolist.filter(function(val){
			  return val.done;
		  }).length;
	  }
  },
  methods:{
	  addTodo(val){
		  console.log(val);
		  this.todolist.push({done:false, todo:val});
	  },
	  subTodo(idx){
		  this.todolist.splice(idx, 1);
	  }
  }
}
</script>

<style>
	.doneStyle {
		text-decoration : line-through;
		color: lightgray;
	}
</style>

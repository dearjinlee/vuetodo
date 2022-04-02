<template>
	<div>
		
    <!-- main.todo -->
    <main class="todo">
        <div class="container">
            <h1>To - Do List</h1>

            <!-- ul.list_add -->
            <ul class="list_add">
                <li class="list_add_tit"><p>등록 하기</p></li>
                <li><p><input type="text"><button>등 록</button></p></li>
            </ul>
            <!--// ul.list_add -->

            <!-- ul.todo_list -->
            <ul class="todo_list">
                <li class="todo_list_tit"><p>할 일</p></li>
                <li class="todo_list_tit"><p>할 일</p></li>

                <li class="del_btn" v-for="(item,index) in todolist" :key="index">
                    <p><input type="checkbox" name="check1" value="">{{ item.todo }}</p>
                    <ul class="todo_list_btn">
                        <li><button>수 정</button></li>
                        <li><button>삭 제</button></li>
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
export default {
  name: 'todolist',
  data: function() {
	return {
		todolist:[
			{todo:"vue.js 공부하기"},
			{todo:"독서 2p 이상"},
			{todo:"보안 과제하기"},
			{todo:"9시 스터디하기"},
			{todo:"과제 채점"},
		]
	}
  },
}
</script>

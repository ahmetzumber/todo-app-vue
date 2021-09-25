<template>
  <div id="cont" class="container" style="margin-top: 20px:">
      <h2>To Do App</h2>
      <Todo @add="addTodo"/>  
      <TodoItem v-for="todo in todos" :key="todo.id" :todoText="todo.text"/>     
  </div>
</template>

<script>
import Todo from './components/Todo.vue'
import TodoItem from './components/TodoItem.vue'

export default { 
  name: "App",
  components: { Todo, TodoItem }, 
  data(){
    return{
      input: '',
      count: 3,
      todos : [
        { id:1, text: 'Learn Vuejs' },
        { id:2, text: 'Learn PostgreSQL' },
        { id:3, text: 'Learn Nodejs' }
      ]
    }
  },
  methods:{
    addTodo(value){
      this.input = value
      if(this.input != null){
        this.todos.push({ id: ++this.count, text: this.input })
      }
    }
  }

};
</script>

<style>
  *{
    margin: 10px;
  }
</style>

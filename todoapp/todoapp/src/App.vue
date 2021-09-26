<template>
  <div id="cont" class="container" style="margin-top: 20px:">
      <h2>To Do App</h2>
      <Todo @add="addTodo"/>  
      <TodoItem v-for="todo in todos" :key="todo.id" :todoText="todo.text" :todoId="todo.id" @remove="removeTodo(todo.id)"/>     
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
    },
    removeTodo(removedItem){
      this.todos = this.todos.filter(todo => todo.id !== removedItem)
    }
  }

};
</script>

<style>
  * {
    padding: 0;
    margin: 10px;
    box-sizing: border-box;
    align-items: center;
    justify-content: center;
  }
  body {
    background: #889EAF;
  }
  .container {
    padding: 30px;
    max-width: 500px;
    margin: 30px auto;
    background: white;
    border-radius: 10px;
    border: 1px solid white;
    box-shadow: 1px 1px 6px 1px rgba(0.3, 0.3, 0.1, 0.3);
  }
</style>

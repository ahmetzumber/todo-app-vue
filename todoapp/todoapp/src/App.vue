<template>
  <div class="container">
    <h3>To Do App</h3>
    <div class="input-group">
      <input v-model="inputTodo" type="text" class="form-control"/>
      <div class="input-group-append">
        <button @click="addToDo" class="btn btn-primary" type="button">Submit</button>
      </div>
    </div>
    <br>
    <ul class="list-group">
        <li :v-for="todo in todos" class="list-group-item d-flex justify-content-between align-items-center">
          {{ todo.text }}
          <button id="remove-btn" class="badge badge-primary badge-pill">X</button>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "App",
  components: {}, 
  data(){
    return{
      todos: [
        { text: 'Learn JavaScript' },
        { text: 'Learn Vue' },
        { text: 'Build something awesome' }
      ]
    }
  },
  methods:{
    addToDo(){
      if(this.inputTodo !== ""){
        this.todos.push({ text: this.inputTodo })
        this.inputTodo = ""
      }
    }
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap");
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  background: lightsteelblue;
}
body {
  font-family: "Poppins", sans-serif;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  background: aliceblue;
  box-shadow: 1px 1px 3px 1px rgba(0.2, 0.2, 0.2, 0.2);
  padding: 30px;
  border-radius: 5px;
}
h3 {
  background: aliceblue;
}
.body {
  background: aliceblue;
}
#remove-btn{
  border: none;
  background: black;
}
</style>

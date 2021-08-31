<template>
  <div class="container">
    <Header title="To Do App"/>
    <Button title="Add To Do"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Header,
    Button
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body {
    font-family: 'Poppins', sans-serif;
  }
  .container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
}
</style>

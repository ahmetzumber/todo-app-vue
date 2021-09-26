<template>
  <div class="container">
    <card :degree="degree" :day="day"/>
  </div>
</template>

<script>
import Card from './components/Card.vue'

export default {
  name: 'App',
  components: {
    Card
  },
  data(){
    return{
      API: "http://api.openweathermap.org/data/2.5/forecast?id=524901&appid=3d5e2980a1680f5d9ec3de64e94bcce6",
      degree: "29°C",
      day: "Monday"
    }
  }
}
</script>

<style>
  * {
    padding: 0;
    margin: 10px;
    box-sizing: border-box;
    align-items: center;
    justify-content: center;
    font-family: 'Quicksand', sans-serif;
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

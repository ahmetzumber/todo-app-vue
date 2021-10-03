<template>
    <div class="formm">
        <input v-model="inputTodo" class="form-control" type="text" v-on:keyup.enter="add">
        <button class="btn btn-primary" @click="add">Add</button>
    </div>
</template>

<script>
export default {
    name: "Todo",
    data(){
        return{
            inputTodo: "",
        }
    },
    methods:{
        add(){
            this.$emit('add',this.inputTodo)
        }
    }
}
</script>

<style >
    .formm {
        display: flex;
        align-items: center;
    }
    button{
        margin: 10px; 
        margin-bottom: 15px
    }
</style>
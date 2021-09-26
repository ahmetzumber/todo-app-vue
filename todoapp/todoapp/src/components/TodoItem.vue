<template>
        <li class="list-group-item d-flex justify-content-between align-items-center">
            {{ todoText }}
            <button @click="remove" class="btn btn-sm btn-danger btn-pill">X</button>
        </li>
</template>

<script>
export default {
    name:'TodoItem',
    props: {
        todoText: String,
    },
    methods:{
        remove(){
            this.$emit('remove')
        }
    }
}
</script>

<style scoped>

</style>
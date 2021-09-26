<template>
    <div>
        <h1>{{ degree }}</h1>
        <h2>{{ day }}</h2>
    </div>
</template>

<script>
export default {
    name: "card",
    props:{
        degree: String,
        day: String
    }

}
</script>

<style scoped>
    div{
        text-align: center;
    }
    h1{
        font-size: 50px;
    }

</style>
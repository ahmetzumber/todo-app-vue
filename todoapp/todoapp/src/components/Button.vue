<template>
    <button class="btn">{{ title }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        title: String
    }
}
</script>
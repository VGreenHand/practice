<template>
    <h3>这是一个组件示范</h3>
    <p>{{ title }}</p>
    <p>age = {{ age }}</p>
    <button @click="sendClickHandel">click</button>
</template>

<script>
    export default {
        name: 'MyComponent',
        props: {
            title: {
                type: String,
                default: '默认标题'
            },
            age: {
                type: Number,
                default: 18
            }
        },
        data() {
            return {
                message: 'This is MyComponent data'
            }
        },
        methods: {
            sendClickHandel(data) {
                this.$emit('send-click', this.message)
            }
        }
    }
</script>

<style>
    h3 {
        margin: 40px 0 0;
        color: red;
    }
</style>
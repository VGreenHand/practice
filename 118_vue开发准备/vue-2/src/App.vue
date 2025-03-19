<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <MyComponent :title="title" :age="age" @send-click="getDataHandle"/>
  <p>{{ msg }}</p>
</template>

<script>
import MyComponent from './components/MyComponent.vue'

export default {
  name: 'App',
  data () {
    return {
      title: 'This is a title',
      age: 20,
      msg:''
    }
  },
  components: {
    MyComponent
  },
  methods: {
    getDataHandle(data) {
      this.msg = data
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
